<script lang="ts">
	import { onMount } from 'svelte';

    // Government agencies and healthcare organizations
    const partners = [
        { name: 'VA', display: 'Department of Veterans Affairs' },
        { name: 'HHS', display: 'Health & Human Services' },
        { name: 'DoD', display: 'Department of Defense' },
        { name: 'CMS', display: 'Centers for Medicare & Medicaid' },
        { name: 'IHS', display: 'Indian Health Service' },
        { name: 'NC DHHS', display: 'North Carolina DHHS' },
        { name: 'Virginia', display: 'Commonwealth of Virginia' },
        { name: 'NY OMH', display: 'NY Office of Mental Health' },
        { name: 'Availity', display: 'Availity' },
        { name: 'CNSI', display: 'CNSI' },
        { name: 'Perspecta', display: 'Perspecta' },
        { name: 'Health First', display: 'Health First' },
    ];

    const caseStudies = [
        {
            tag: 'Case Study',
            title: 'VA VistA EHR Deployment',
            desc: 'Successfully deployed VA\'s open source VistA EHR/EMR across 24 inpatient psychiatric hospitals for NYS Office of Mental Health',
            img: '/generated/image-va-hospital-staff-using-electronic-healt-1767710019486-3.webp',
            bg: 'bg-gray-50'
        },
        {
            tag: 'Innovation',
            title: 'Graph-Based Fraud Detection',
            desc: 'Selected as CMS finalist for graph-based approach to Medicare Fee-for-Service fraud detection in Crushing Fraud Competition',
            img: '/generated/image-government-data-center-with-servers-and--1767710016270-2.webp',
            bg: 'bg-primary-50'
        },
        {
            tag: 'Case Study',
            title: 'Virginia T-MSIS Implementation',
            desc: 'First state to go live with T-MSIS implementation, enabling critical Medicaid data reporting and interoperability',
            img: '/generated/image-federal-government-it-professionals-coll-1767710009516-0.webp',
            bg: 'bg-gray-50'
        },
        {
            tag: 'Solution',
            title: 'FHIR Interoperability Platform',
            desc: 'Developed custom FHIR servers in one-third the time for CNSI, providing subject matter expertise and agile operations guidance',
            img: '/generated/image-government-data-center-with-servers-and--1767710016270-2.webp',
            bg: 'bg-primary-50'
        }
    ];

    const testimonials = [
        {
            quote: "Outstanding technical quality in designs enabled excellent public sector health IT applications. A rare level of performance.",
            author: "Mike O'Neill",
            role: "CEO",
            company: "MedicaSoft",
            img: "/generated/image-healthcare-it-director-reviewing-patient-1767710013268-1.webp"
        },
        {
            quote: "Completed complicated data mapping for claims systems unification with minimal guidance needed.",
            author: "William Walders",
            role: "CIO",
            company: "Health First",
            img: "/generated/image-healthcare-it-director-reviewing-patient-1767710013268-1.webp"
        },
        {
            quote: "Developed custom FHIR servers in one-third the time, provided FHIR subject matter expertise and guided teams toward agile operations.",
            author: "Sashi Ravipati",
            role: "SVP",
            company: "CNSI",
            img: "/generated/image-healthcare-it-director-reviewing-patient-1767710013268-1.webp"
        }
    ];
</script>

<div class="min-h-screen bg-white text-gray-900 font-sans selection:bg-gray-200">
    <!-- Header -->
    <header class="fixed top-0 left-0 right-0 z-50 bg-white/90 backdrop-blur-sm border-b border-gray-100">
        <div class="max-w-[1600px] mx-auto px-6 py-6 flex justify-between items-center">
            <div class="flex items-center gap-3">
                <div class="w-8 h-8 text-primary-600">
                    <svg viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                        <path fill-rule="evenodd" clip-rule="evenodd" d="M6.99251 12.196C6.85314 12.5757 6.62925 12.9208 6.33682 13.2067H6.33835C6.00191 13.5351 5.58566 13.7756 5.12816 13.9059C4.67065 14.0362 4.18671 14.0522 3.72118 13.9523C3.25564 13.8524 2.82357 13.64 2.46501 13.3345C2.10645 13.0291 1.83299 12.6406 1.66998 12.2051C1.50697 11.7696 1.45969 11.3012 1.5325 10.8432C1.60532 10.3852 1.79587 9.95244 2.08653 9.58516C2.37718 9.21781 2.75852 8.9277 3.1952 8.74177C3.63188 8.55585 4.10979 8.48002 4.58462 8.52142L4.57074 8.50792C5.0567 8.54782 5.54575 8.48407 6.00378 8.32124C6.4618 8.15846 6.87776 7.90043 7.2226 7.56521C7.56746 7.22998 7.83285 6.82564 8.00036 6.38041C8.16786 5.93517 8.23344 5.45976 8.1924 4.98737L8.20628 5.00087C8.15181 4.43594 8.27796 3.86844 8.56753 3.37575C8.85701 2.88307 9.29579 2.48919 9.82407 2.24782C10.3523 2.00645 10.9443 1.92933 11.5192 2.02701C12.0942 2.12467 12.6243 2.39237 13.037 2.79358C13.4497 3.19479 13.7251 3.70999 13.8256 4.26892C13.926 4.82785 13.8467 5.4033 13.5984 5.9168C13.3501 6.4303 12.9449 6.85685 12.4381 7.13828C11.9313 7.41971 11.3474 7.54233 10.7663 7.4894L10.781 7.5029C10.2949 7.46279 9.80563 7.52632 9.34741 7.68904C8.88919 7.85176 8.47309 8.10975 8.12805 8.44499C7.78301 8.78025 7.51742 9.18466 7.34983 9.63001C7.18224 10.0754 7.11669 10.551 7.15774 11.0235L7.14309 11.01C7.1833 11.4112 7.13189 11.8162 6.99251 12.196ZM11.5077 14.7121L11.493 14.6986C11.9061 14.739 12.3232 14.6897 12.7143 14.5543C13.1053 14.4188 13.4605 14.2007 13.7542 13.9154C14.0477 13.6302 14.2726 13.285 14.4121 12.905C14.5518 12.525 14.6028 12.1196 14.5615 11.718L14.5762 11.7315C14.5351 11.2591 14.6007 10.7838 14.7681 10.3385C14.9356 9.89327 15.2011 9.48893 15.5459 9.15368C15.8908 8.8185 16.3068 8.56042 16.7648 8.39767C17.2228 8.23481 17.7118 8.17111 18.1978 8.21099L18.1832 8.19749C18.7645 8.25059 19.3485 8.12801 19.8556 7.84656C20.3627 7.56511 20.7681 7.13845 21.0165 6.62479C21.265 6.11114 21.3444 5.53548 21.2439 4.97634C21.1435 4.4172 20.868 3.9018 20.4551 3.50044C20.0422 3.09909 19.512 2.8313 18.9368 2.73364C18.3616 2.63596 17.7695 2.71315 17.241 2.95467C16.7126 3.19618 16.2737 3.59027 15.9842 4.08319C15.6946 4.57609 15.5685 5.14383 15.6232 5.70895L15.6093 5.6947C15.6504 6.16712 15.585 6.64259 15.4175 7.08788C15.2501 7.53318 14.9846 7.93758 14.6398 8.27287C14.2949 8.60805 13.8789 8.86612 13.4208 9.02888C12.9627 9.19163 12.4736 9.25523 11.9876 9.21526L12.0015 9.22951C11.5885 9.18908 11.1713 9.23836 10.7803 9.37381C10.3893 9.50919 10.034 9.72744 9.74039 10.0127C9.44674 10.2979 9.22199 10.6431 9.08234 11.0231C8.94276 11.4031 8.89176 11.8085 8.93304 12.2101L8.91915 12.1966C8.96005 12.6689 8.89439 13.1443 8.72688 13.5895C8.5593 14.0346 8.29389 14.4389 7.94908 14.7741C7.60425 15.1093 7.18835 15.3673 6.73039 15.5302C6.27242 15.693 5.78342 15.7569 5.29749 15.7171L5.31138 15.7306C4.73003 15.6775 4.14599 15.8001 3.63892 16.0815C3.13186 16.363 2.72644 16.7896 2.478 17.3033C2.22954 17.817 2.15013 18.3926 2.25061 18.9518C2.35109 19.5109 2.62657 20.0263 3.03945 20.4276C3.45234 20.829 3.98253 21.0968 4.55773 21.1944C5.13293 21.2921 5.72512 21.2149 6.25353 20.9734C6.78193 20.7319 7.22085 20.3379 7.51038 19.8449C7.79994 19.352 7.92601 18.7843 7.87139 18.2191L7.88605 18.2326C7.845 17.7602 7.91058 17.2849 8.07809 16.8396C8.24551 16.3944 8.511 15.99 8.85581 15.6548C9.20069 15.3196 9.61664 15.0615 10.0746 14.8988C10.5327 14.7359 11.0217 14.6722 11.5077 14.7121ZM17.1996 10.7633C16.9071 11.0493 16.6832 11.3944 16.5437 11.7741C16.4042 12.1538 16.3526 12.5587 16.3925 12.9601L16.3786 12.9466C16.4197 13.419 16.3541 13.8944 16.1866 14.3396C16.0191 14.7849 15.7537 15.1892 15.4089 15.5244C15.064 15.8596 14.648 16.1177 14.19 16.2804C13.732 16.4433 13.2429 16.507 12.757 16.4671L12.7708 16.4806C12.1896 16.4281 11.6057 16.551 11.0989 16.8328C10.5921 17.1145 10.1871 17.5414 9.93902 18.0551C9.69097 18.5689 9.61188 19.1444 9.71265 19.7035C9.81349 20.2625 10.0892 20.7777 10.5022 21.1788C10.9152 21.5799 11.4454 21.8474 12.0205 21.9448C12.5957 22.0423 13.1877 21.9649 13.716 21.7234C14.2443 21.4817 14.683 21.0877 14.9724 20.5947C15.2618 20.1018 15.3878 19.5342 15.3332 18.9692L15.3478 18.9827C15.3068 18.5103 15.3723 18.0349 15.5398 17.5896C15.7073 17.1444 15.9728 16.7401 16.3176 16.4048C16.6625 16.0696 17.0784 15.8115 17.5364 15.6488C17.9945 15.486 18.4835 15.4222 18.9695 15.4621L18.9548 15.4486C19.4296 15.4901 19.9076 15.4144 20.3444 15.2286C20.7811 15.0427 21.1625 14.7527 21.4533 14.3854C21.744 14.0181 21.9347 13.5854 22.0075 13.1274C22.0805 12.6694 22.0332 12.2009 21.8703 11.7653C21.7073 11.3298 21.4339 10.9413 21.0754 10.6358C20.7168 10.3303 20.2848 10.1178 19.8192 10.0179C19.3536 9.91795 18.8697 9.93385 18.4121 10.0641C17.9546 10.1945 17.5383 10.4349 17.2019 10.7633H17.1996Z" fill="currentColor" />
                    </svg>
                </div>
                <a href="/" class="text-lg font-semibold text-gray-900">
                    Amida
                </a>
            </div>
            <div>
                <a href="#contact" class="bg-primary-600 text-white px-5 py-2.5 text-xs font-medium rounded-sm hover:bg-primary-700 transition-colors">
                    Contact Us
                </a>
            </div>
        </div>
    </header>

    <main class="pt-32 pb-20">
        <div class="max-w-[1600px] mx-auto px-6 grid grid-cols-12 gap-8">
            <!-- Sidebar Navigation -->
            <div class="col-span-2 hidden lg:block sticky top-32 h-fit">
                <nav class="flex flex-col space-y-3 text-xs text-gray-500 font-medium">
                    <a href="#" class="text-gray-900">Home</a>
                    <a href="#solutions" class="hover:text-gray-900 transition-colors">Solutions</a>
                    <a href="#capabilities" class="hover:text-gray-900 transition-colors">Capabilities</a>
                    <a href="#clients" class="hover:text-gray-900 transition-colors">Clients</a>
                    <a href="#about" class="hover:text-gray-900 transition-colors">About</a>
                </nav>
            </div>

            <!-- Main Content Area -->
            <div class="col-span-12 lg:col-span-10 space-y-32">
                
                <!-- Hero Section -->
                <section class="relative">
                    <div class="relative w-full h-[600px] overflow-hidden rounded-sm">
                        <img src="/generated/image-federal-government-it-professionals-coll-1767710009516-0.webp" alt="Federal government IT operations" class="absolute inset-0 w-full h-full object-cover" />
                        
                        <div class="absolute inset-0 bg-gradient-to-r from-gray-900/80 to-gray-900/40"></div>
                        
                        <div class="absolute inset-0 flex flex-col items-center justify-center p-12 text-center">
                            <h1 class="text-4xl md:text-5xl font-normal text-white mb-12 max-w-3xl leading-tight">
                                Unifying fragmented government data<br>through automated interoperability
                            </h1>

                            <!-- Logos Card -->
                            <div class="bg-white/95 backdrop-blur-sm p-8 rounded-sm shadow-sm max-w-4xl w-full">
                                <p class="text-[10px] text-gray-600 mb-6 uppercase tracking-wide">
                                    Trusted by federal agencies, state governments, and healthcare organizations
                                </p>
                                <div class="grid grid-cols-3 md:grid-cols-6 gap-6 items-center justify-items-center">
                                    {#each partners as partner}
                                        <div class="h-8 flex items-center justify-center">
                                            <span class="text-[9px] font-semibold text-gray-700 text-center leading-tight">{partner.name}</span>
                                        </div>
                                    {/each}
                                </div>
                            </div>
                        </div>
                    </div>
                </section>

                <!-- How Amida Works Section -->
                <section id="solutions">
                    <div class="flex justify-between items-baseline mb-24 border-b border-gray-100 pb-4">
                        <h2 class="text-3xl font-light text-gray-900 max-w-xl leading-tight">
                            How Amida solves government data interoperability
                        </h2>
                        <span class="text-[10px] text-gray-400 uppercase tracking-wider">Our Approach</span>
                    </div>

                    <div class="relative min-h-[800px]">
                        <!-- Diagram -->
                        <div class="absolute right-0 top-0 w-1/2 p-8 bg-gray-50 rounded-sm">
                            <div class="text-[10px] text-gray-500 mb-4 uppercase tracking-wide">Automated Interoperability Engine</div>
                            <div class="flex items-center justify-between gap-4">
                                <div class="w-32 h-32 bg-gray-800 text-white flex flex-col items-center justify-center p-4 rounded-sm">
                                    <div class="mb-2">
                                        <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 7v10c0 2.21 3.582 4 8 4s8-1.79 8-4V7M4 7c0 2.21 3.582 4 8 4s8-1.79 8-4M4 7c0-2.21 3.582-4 8-4s8 1.79 8 4"></path></svg>
                                    </div>
                                    <span class="text-[9px] uppercase tracking-wider text-center">Legacy System A</span>
                                </div>
                                
                                <div class="flex-1 h-32 bg-primary-100/50 border border-primary-200 rounded-sm flex flex-col items-center justify-center relative">
                                    <span class="text-[10px] text-gray-600 uppercase absolute top-2 left-4">Graph Architecture</span>
                                    <div class="w-full border-t border-dashed border-gray-400 absolute top-1/2"></div>
                                    
                                    <!-- Amida Icon -->
                                    <div class="absolute -bottom-6 bg-white border border-gray-200 p-2 shadow-sm rounded-sm flex items-center gap-2">
                                        <div class="w-8 h-8 text-primary-600">
                                            <svg viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                                                <path fill-rule="evenodd" clip-rule="evenodd" d="M6.99251 12.196C6.85314 12.5757 6.62925 12.9208 6.33682 13.2067H6.33835C6.00191 13.5351 5.58566 13.7756 5.12816 13.9059C4.67065 14.0362 4.18671 14.0522 3.72118 13.9523C3.25564 13.8524 2.82357 13.64 2.46501 13.3345C2.10645 13.0291 1.83299 12.6406 1.66998 12.2051C1.50697 11.7696 1.45969 11.3012 1.5325 10.8432C1.60532 10.3852 1.79587 9.95244 2.08653 9.58516C2.37718 9.21781 2.75852 8.9277 3.1952 8.74177C3.63188 8.55585 4.10979 8.48002 4.58462 8.52142L4.57074 8.50792C5.0567 8.54782 5.54575 8.48407 6.00378 8.32124C6.4618 8.15846 6.87776 7.90043 7.2226 7.56521C7.56746 7.22998 7.83285 6.82564 8.00036 6.38041C8.16786 5.93517 8.23344 5.45976 8.1924 4.98737L8.20628 5.00087C8.15181 4.43594 8.27796 3.86844 8.56753 3.37575C8.85701 2.88307 9.29579 2.48919 9.82407 2.24782C10.3523 2.00645 10.9443 1.92933 11.5192 2.02701C12.0942 2.12467 12.6243 2.39237 13.037 2.79358C13.4497 3.19479 13.7251 3.70999 13.8256 4.26892C13.926 4.82785 13.8467 5.4033 13.5984 5.9168C13.3501 6.4303 12.9449 6.85685 12.4381 7.13828C11.9313 7.41971 11.3474 7.54233 10.7663 7.4894L10.781 7.5029C10.2949 7.46279 9.80563 7.52632 9.34741 7.68904C8.88919 7.85176 8.47309 8.10975 8.12805 8.44499C7.78301 8.78025 7.51742 9.18466 7.34983 9.63001C7.18224 10.0754 7.11669 10.551 7.15774 11.0235L7.14309 11.01C7.1833 11.4112 7.13189 11.8162 6.99251 12.196Z" fill="currentColor" />
                                            </svg>
                                        </div>
                                        <div class="text-[8px] leading-tight text-gray-600 font-semibold">
                                            AMIDA<br>PLATFORM
                                        </div>
                                    </div>
                                </div>

                                <div class="w-32 h-32 bg-gray-800 text-white flex flex-col items-center justify-center p-4 rounded-sm">
                                    <div class="mb-2">
                                        <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 7v10c0 2.21 3.582 4 8 4s8-1.79 8-4V7M4 7c0 2.21 3.582 4 8 4s8-1.79 8-4M4 7c0-2.21 3.582-4 8-4s8 1.79 8 4"></path></svg>
                                    </div>
                                    <span class="text-[9px] uppercase tracking-wider text-center">Legacy System B</span>
                                </div>
                            </div>
                        </div>

                        <!-- Text Blocks -->
                        <div class="absolute left-0 top-[200px] max-w-md">
                            <div class="flex gap-4">
                                <span class="bg-primary-600 text-white w-5 h-5 flex items-center justify-center text-xs font-medium shrink-0 rounded-sm">1</span>
                                <p class="text-sm text-gray-600 leading-relaxed">
                                    Federal IT leaders face fragmented legacy databases across departments. Each system speaks a different language, making data sharing nearly impossible.
                                </p>
                            </div>
                        </div>

                        <div class="absolute left-0 top-[400px] max-w-md">
                            <div class="flex gap-4">
                                <span class="bg-primary-600 text-white w-5 h-5 flex items-center justify-center text-xs font-medium shrink-0 rounded-sm">2</span>
                                <p class="text-sm text-gray-600 leading-relaxed">
                                    Amida's automated interoperability engines use graph-based architecture to connect disparate systems, enabling seamless data exchange without replacing existing infrastructure.
                                </p>
                            </div>
                        </div>

                        <div class="absolute left-0 top-[600px] max-w-md">
                            <div class="flex gap-4">
                                <span class="bg-primary-600 text-white w-5 h-5 flex items-center justify-center text-xs font-medium shrink-0 rounded-sm">3</span>
                                <p class="text-sm text-gray-600 leading-relaxed">
                                    HIPAA-compliant and NIST-aligned, our solutions meet the strictest government security standards while delivering real-time data interoperability.
                                </p>
                            </div>
                        </div>
                    </div>
                </section>

                <!-- About Amida Section -->
                <section id="about">
                    <div class="flex justify-between items-baseline mb-16 border-b border-gray-100 pb-4">
                        <h2 class="text-3xl font-light text-gray-900">
                            Born from government innovation
                        </h2>
                        <span class="text-[10px] text-gray-400 uppercase tracking-wider">Our Story</span>
                    </div>

                    <div class="grid grid-cols-1 md:grid-cols-3 gap-12 text-sm leading-relaxed text-gray-600 mb-24">
                        <div class="space-y-6">
                            <p>
                                Founded in 2013 by three Presidential Innovation Fellows who saw firsthand the data challenges plaguing federal agencies.
                            </p>
                            <p>
                                Peter L. Levin, former Chief Technology Officer at the Department of Veterans Affairs, led health record modernization initiatives that revealed the critical need for true data interoperability.
                            </p>
                        </div>
                        <div class="space-y-6">
                            <p>
                                Government agencies manage some of the world's most critical data—from veteran healthcare records to Medicaid claims—but legacy systems can't communicate. The result: fragmented care, duplicated efforts, and billions in wasted spending.
                            </p>
                            <p>
                                We built Amida to solve the hardest problems in data management and interoperability. Our graph-based architecture and FHIR expertise enable reliable exchange of sensitive information across systems that were never designed to work together.
                            </p>
                        </div>
                        <div class="space-y-6">
                            <p>
                                Today, we serve federal health agencies, state Medicaid programs, and healthcare organizations across 24 states. Our solutions are HIPAA-compliant, ISO 9001-2015 certified, and aligned with NIST 800-171 controls.
                            </p>
                            <p>
                                Led by CEO Mukundan Srinivasan and CTO Rajesh K. Krishnasamy, with guidance from a board including former Under Secretary of Defense Michèle Flournoy, we continue to tackle government's toughest data challenges.
                            </p>
                        </div>
                    </div>

                    <!-- Certifications & Credentials -->
                    <div class="bg-gray-50 rounded-sm p-8">
                        <span class="text-[10px] text-gray-400 uppercase tracking-wider block mb-6">Certifications & Credentials</span>
                        <div class="grid grid-cols-2 md:grid-cols-4 gap-6 text-xs text-gray-700">
                            <div class="flex flex-col gap-1">
                                <span class="font-semibold">HIPAA Compliant</span>
                                <span class="text-gray-500">Healthcare data security</span>
                            </div>
                            <div class="flex flex-col gap-1">
                                <span class="font-semibold">ISO 9001-2015</span>
                                <span class="text-gray-500">Quality management</span>
                            </div>
                            <div class="flex flex-col gap-1">
                                <span class="font-semibold">NIST 800-171</span>
                                <span class="text-gray-500">Federal security standards</span>
                            </div>
                            <div class="flex flex-col gap-1">
                                <span class="font-semibold">GSA Schedule</span>
                                <span class="text-gray-500">47QTCA18D00CN</span>
                            </div>
                        </div>
                    </div>
                </section>

                <!-- Core Capabilities Dark Section -->
                <section id="capabilities" class="bg-gray-900 text-white rounded-sm overflow-hidden relative min-h-[500px] flex items-center">
                    <!-- Background Graphic -->
                    <div class="absolute inset-0 opacity-20">
                        <div class="absolute bottom-0 left-0 right-0 h-64 bg-gradient-to-t from-primary-900/30 to-transparent"></div>
                        <svg class="absolute bottom-0 w-full h-full text-primary-900/20" viewBox="0 0 100 100" preserveAspectRatio="none">
                            <circle cx="20" cy="80" r="2" fill="currentColor" opacity="0.5"/>
                            <circle cx="40" cy="70" r="2" fill="currentColor" opacity="0.5"/>
                            <circle cx="60" cy="75" r="2" fill="currentColor" opacity="0.5"/>
                            <circle cx="80" cy="85" r="2" fill="currentColor" opacity="0.5"/>
                            <line x1="20" y1="80" x2="40" y2="70" stroke="currentColor" stroke-width="0.5" opacity="0.3"/>
                            <line x1="40" y1="70" x2="60" y2="75" stroke="currentColor" stroke-width="0.5" opacity="0.3"/>
                            <line x1="60" y1="75" x2="80" y2="85" stroke="currentColor" stroke-width="0.5" opacity="0.3"/>
                        </svg>
                    </div>

                    <div class="relative z-10 p-16 w-full">
                        <div class="mb-12">
                            <h2 class="text-3xl font-light mb-6">
                                Core capabilities for government<br>data interoperability
                            </h2>
                            <p class="text-sm text-gray-400 max-w-2xl">
                                From FHIR implementation to graph-based architectures, we deliver the technical expertise federal agencies need.
                            </p>
                        </div>
                        
                        <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                            <div class="bg-white/5 backdrop-blur-sm border border-white/10 p-6 rounded-sm">
                                <div class="w-10 h-10 bg-primary-600/20 rounded-sm flex items-center justify-center mb-4">
                                    <svg class="w-5 h-5 text-primary-400" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 10V3L4 14h7v7l9-11h-7z"></path></svg>
                                </div>
                                <h3 class="text-lg font-medium mb-2">FHIR Expertise</h3>
                                <p class="text-xs text-gray-400 leading-relaxed">
                                    Deep expertise in Fast Healthcare Interoperability Resources (FHIR) standards, enabling modern healthcare data exchange across legacy systems.
                                </p>
                            </div>

                            <div class="bg-white/5 backdrop-blur-sm border border-white/10 p-6 rounded-sm">
                                <div class="w-10 h-10 bg-primary-600/20 rounded-sm flex items-center justify-center mb-4">
                                    <svg class="w-5 h-5 text-primary-400" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 3v2m6-2v2M9 19v2m6-2v2M5 9H3m2 6H3m18-6h-2m2 6h-2M7 19h10a2 2 0 002-2V7a2 2 0 00-2-2H7a2 2 0 00-2 2v10a2 2 0 002 2zM9 9h6v6H9V9z"></path></svg>
                                </div>
                                <h3 class="text-lg font-medium mb-2">Graph-Based Architecture</h3>
                                <p class="text-xs text-gray-400 leading-relaxed">
                                    Restructure fragmented data using graph databases to improve accuracy, enable pattern recognition, and accelerate decision-making.
                                </p>
                            </div>

                            <div class="bg-white/5 backdrop-blur-sm border border-white/10 p-6 rounded-sm">
                                <div class="w-10 h-10 bg-primary-600/20 rounded-sm flex items-center justify-center mb-4">
                                    <svg class="w-5 h-5 text-primary-400" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 15v2m-6 4h12a2 2 0 002-2v-6a2 2 0 00-2-2H6a2 2 0 00-2 2v6a2 2 0 002 2zm10-10V7a4 4 0 00-8 0v4h8z"></path></svg>
                                </div>
                                <h3 class="text-lg font-medium mb-2">Security & Compliance</h3>
                                <p class="text-xs text-gray-400 leading-relaxed">
                                    HIPAA-compliant, ISO 9001-2015 certified, and NIST 800-171 aligned. Built for the strictest government security requirements.
                                </p>
                            </div>

                            <div class="bg-white/5 backdrop-blur-sm border border-white/10 p-6 rounded-sm">
                                <div class="w-10 h-10 bg-primary-600/20 rounded-sm flex items-center justify-center mb-4">
                                    <svg class="w-5 h-5 text-primary-400" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9.75 17L9 20l-1 1h8l-1-1-.75-3M3 13h18M5 17h14a2 2 0 002-2V5a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"></path></svg>
                                </div>
                                <h3 class="text-lg font-medium mb-2">VistA EHR Deployment</h3>
                                <p class="text-xs text-gray-400 leading-relaxed">
                                    Proven track record deploying VA's open source VistA electronic health record system across state psychiatric facilities.
                                </p>
                            </div>

                            <div class="bg-white/5 backdrop-blur-sm border border-white/10 p-6 rounded-sm">
                                <div class="w-10 h-10 bg-primary-600/20 rounded-sm flex items-center justify-center mb-4">
                                    <svg class="w-5 h-5 text-primary-400" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 19v-6a2 2 0 00-2-2H5a2 2 0 00-2 2v6a2 2 0 002 2h2a2 2 0 002-2zm0 0V9a2 2 0 012-2h2a2 2 0 012 2v10m-6 0a2 2 0 002 2h2a2 2 0 002-2m0 0V5a2 2 0 012-2h2a2 2 0 012 2v14a2 2 0 01-2 2h-2a2 2 0 01-2-2z"></path></svg>
                                </div>
                                <h3 class="text-lg font-medium mb-2">AI/ML for Data Analysis</h3>
                                <p class="text-xs text-gray-400 leading-relaxed">
                                    Automated metadata categorization and fraud detection using machine learning to derive insights from complex government datasets.
                                </p>
                            </div>

                            <div class="bg-white/5 backdrop-blur-sm border border-white/10 p-6 rounded-sm">
                                <div class="w-10 h-10 bg-primary-600/20 rounded-sm flex items-center justify-center mb-4">
                                    <svg class="w-5 h-5 text-primary-400" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 7v10c0 2.21 3.582 4 8 4s8-1.79 8-4V7M4 7c0 2.21 3.582 4 8 4s8-1.79 8-4M4 7c0-2.21 3.582-4 8-4s8 1.79 8 4m0 5c0 2.21-3.582 4-8 4s-8-1.79-8-4"></path></svg>
                                </div>
                                <h3 class="text-lg font-medium mb-2">Medicaid Modernization</h3>
                                <p class="text-xs text-gray-400 leading-relaxed">
                                    T-MSIS implementation and MMIS modernization expertise. Virginia was the first state to go live with our T-MSIS solution.
                                </p>
                            </div>
                        </div>
                    </div>
                </section>

                <!-- Testimonials -->
                <section id="clients">
                    <div class="flex justify-between items-baseline mb-16 border-b border-gray-100 pb-4">
                        <h2 class="text-3xl font-light text-gray-900">
                            Trusted by government and healthcare leaders
                        </h2>
                        <span class="text-[10px] text-gray-400 uppercase tracking-wider">Client Testimonials</span>
                    </div>

                    <div class="relative">
                        <div class="flex gap-8 overflow-hidden">
                            <div class="w-full md:w-[800px] shrink-0 bg-gray-50 flex">
                                <div class="w-1/3 shrink-0">
                                    <img src="/generated/image-healthcare-it-director-reviewing-patient-1767710013268-1.webp" alt="Healthcare IT Leader" class="w-full h-full object-cover" />
                                </div>
                                <div class="w-2/3 p-12 flex flex-col justify-center">
                                    <blockquote class="text-xl font-light leading-relaxed mb-8">
                                        "{testimonials[0].quote}"
                                    </blockquote>
                                    <div class="flex items-center gap-2 mb-2">
                                        <div class="w-1 h-8 bg-primary-600"></div>
                                        <span class="text-xs font-semibold text-gray-600">{testimonials[0].company}</span>
                                    </div>
                                    <div>
                                        <div class="font-medium">{testimonials[0].author}</div>
                                        <div class="text-xs text-gray-500">{testimonials[0].role}</div>
                                    </div>
                                </div>
                            </div>
                            <!-- Next slide preview -->
                            <div class="w-1/3 shrink-0 opacity-50 bg-gray-100 flex items-center justify-center">
                                <div class="text-center p-6">
                                    <p class="text-sm text-gray-600 mb-4">"{testimonials[1].quote.substring(0, 60)}..."</p>
                                    <p class="text-xs font-semibold text-gray-700">{testimonials[1].author}</p>
                                    <p class="text-xs text-gray-500">{testimonials[1].company}</p>
                                </div>
                            </div>
                        </div>
                        
                        <!-- Navigation Button -->
                        <button class="absolute top-0 right-0 -mt-12 w-8 h-8 bg-primary-600 text-white flex items-center justify-center hover:bg-primary-700 rounded-sm">
                            <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7"></path></svg>
                        </button>
                    </div>

                    <!-- Additional Client Quotes -->
                    <div class="mt-16 grid grid-cols-1 md:grid-cols-2 gap-8">
                        <div class="border-l-2 border-primary-600 pl-6 py-4">
                            <p class="text-sm text-gray-600 mb-4 leading-relaxed">
                                "Built proof-of-concept harmonization engine for duplicate patient record matching, reducing fragmentation in VA care."
                            </p>
                            <p class="text-xs font-semibold text-gray-700">Bo Dagnall, Perspecta</p>
                        </div>
                        <div class="border-l-2 border-primary-600 pl-6 py-4">
                            <p class="text-sm text-gray-600 mb-4 leading-relaxed">
                                "Developed tool to search massive CCD inventory for HEDIS scores, eliminating chart chasing and lowering costs."
                            </p>
                            <p class="text-xs font-semibold text-gray-700">Russ Thomas, CEO, Availity</p>
                        </div>
                    </div>
                </section>

                <!-- Case Studies / Solutions -->
                <section>
                    <div class="flex justify-between items-baseline mb-16 border-b border-gray-100 pb-4">
                        <h2 class="text-3xl font-light text-gray-900">
                            Solutions in action
                        </h2>
                        <span class="text-[10px] text-gray-400 uppercase tracking-wider">Case Studies</span>
                    </div>

                    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8">
                        {#each caseStudies as study}
                            <div class="group cursor-pointer">
                                <div class="relative aspect-square mb-6 overflow-hidden {study.bg} rounded-sm">
                                    <img src="{study.img}" alt="{study.title}" class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-300" />
                                    <span class="absolute top-4 left-4 text-[10px] uppercase tracking-wider bg-white/90 px-2 py-1 backdrop-blur-sm text-gray-800 font-medium">{study.tag}</span>
                                </div>
                                <h3 class="text-lg font-normal mb-3 leading-tight group-hover:text-primary-700 transition-colors">
                                    {study.title}
                                </h3>
                                <p class="text-xs text-gray-500 mb-4 leading-relaxed">
                                    {study.desc}
                                </p>
                                <a href="#" class="text-xs font-medium text-primary-600 hover:text-primary-700 underline decoration-1 underline-offset-4">Learn more</a>
                            </div>
                        {/each}
                    </div>
                </section>

            </div>
        </div>
    </main>

    <!-- Footer -->
    <footer id="contact" class="bg-white pt-32 pb-12 border-t border-gray-100 relative overflow-hidden">
        <!-- Large Background Watermark -->
        <div class="absolute left-0 bottom-0 text-[20vw] font-bold text-gray-50 leading-none select-none pointer-events-none -mb-12 -ml-12">
            AMIDA
        </div>

        <div class="max-w-[1600px] mx-auto px-6 relative z-10">
            <div class="flex flex-col md:flex-row justify-between items-start md:items-center mb-24 gap-8">
                <div>
                    <h3 class="text-2xl font-light text-gray-900 mb-4">Ready to modernize your data infrastructure?</h3>
                    <p class="text-sm text-gray-600">Let's discuss how Amida can solve your interoperability challenges.</p>
                </div>
                <div class="flex flex-col gap-3">
                    <a href="tel:+12027351798" class="text-sm font-medium text-primary-600 hover:text-primary-700">(202) 735-1798</a>
                    <a href="mailto:info@amida.com" class="text-sm font-medium text-primary-600 hover:text-primary-700">info@amida.com</a>
                </div>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-12 gap-8 items-end">
                <div class="md:col-span-6">
                    <!-- Logo -->
                    <div class="flex items-center gap-3 mb-6">
                        <div class="w-8 h-8 text-primary-600">
                            <svg viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                                <path fill-rule="evenodd" clip-rule="evenodd" d="M6.99251 12.196C6.85314 12.5757 6.62925 12.9208 6.33682 13.2067H6.33835C6.00191 13.5351 5.58566 13.7756 5.12816 13.9059C4.67065 14.0362 4.18671 14.0522 3.72118 13.9523C3.25564 13.8524 2.82357 13.64 2.46501 13.3345C2.10645 13.0291 1.83299 12.6406 1.66998 12.2051C1.50697 11.7696 1.45969 11.3012 1.5325 10.8432C1.60532 10.3852 1.79587 9.95244 2.08653 9.58516C2.37718 9.21781 2.75852 8.9277 3.1952 8.74177C3.63188 8.55585 4.10979 8.48002 4.58462 8.52142L4.57074 8.50792C5.0567 8.54782 5.54575 8.48407 6.00378 8.32124C6.4618 8.15846 6.87776 7.90043 7.2226 7.56521C7.56746 7.22998 7.83285 6.82564 8.00036 6.38041C8.16786 5.93517 8.23344 5.45976 8.1924 4.98737L8.20628 5.00087C8.15181 4.43594 8.27796 3.86844 8.56753 3.37575C8.85701 2.88307 9.29579 2.48919 9.82407 2.24782C10.3523 2.00645 10.9443 1.92933 11.5192 2.02701C12.0942 2.12467 12.6243 2.39237 13.037 2.79358C13.4497 3.19479 13.7251 3.70999 13.8256 4.26892C13.926 4.82785 13.8467 5.4033 13.5984 5.9168C13.3501 6.4303 12.9449 6.85685 12.4381 7.13828C11.9313 7.41971 11.3474 7.54233 10.7663 7.4894L10.781 7.5029C10.2949 7.46279 9.80563 7.52632 9.34741 7.68904C8.88919 7.85176 8.47309 8.10975 8.12805 8.44499C7.78301 8.78025 7.51742 9.18466 7.34983 9.63001C7.18224 10.0754 7.11669 10.551 7.15774 11.0235L7.14309 11.01C7.1833 11.4112 7.13189 11.8162 6.99251 12.196Z" fill="currentColor" />
                            </svg>
                        </div>
                        <div class="text-lg font-semibold text-gray-900">
                            Amida
                        </div>
                    </div>
                    <div class="text-xs text-gray-500 space-y-1">
                        <p>1133 15th Street NW, Suite 703</p>
                        <p>Washington, DC 20005</p>
                        <p class="pt-2">GSA Schedule: 47QTCA18D00CN</p>
                    </div>
                </div>
                
                <div class="md:col-span-6 flex flex-col md:flex-row justify-between items-start md:items-end gap-8">
                    <div class="text-[10px] text-gray-400">
                        © 2025 Amida Technology Solutions, Inc.
                    </div>
                    
                    <div class="flex gap-8 text-[10px] font-medium uppercase tracking-wide">
                        <div class="flex flex-col gap-2">
                            <a href="#about" class="hover:text-primary-600 transition-colors">About</a>
                            <a href="#capabilities" class="hover:text-primary-600 transition-colors">Capabilities</a>
                            <a href="#clients" class="hover:text-primary-600 transition-colors">Clients</a>
                        </div>
                        <div class="flex flex-col gap-2">
                            <a href="#contact" class="hover:text-primary-600 transition-colors">Contact</a>
                            <a href="#" class="hover:text-primary-600 transition-colors">Careers</a>
                            <a href="#" class="hover:text-primary-600 transition-colors">Privacy</a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </footer>
</div>

<style>
    /* Custom scrollbar hide for clean look */
    ::-webkit-scrollbar {
        width: 0px;
        background: transparent;
    }
</style>

