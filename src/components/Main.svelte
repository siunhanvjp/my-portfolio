<script>
    import Step from "./Step.svelte";

    let steps = [
        {
            name: "Alime-Tinder",
            imgSrc: "images/tinder.png",
            github: "https://github.com/siunhanvjp/alime-tinder",
            webUrl: "https://alime-tinder.web.app/",
            description: "Welcome to Alime-Tinder, where anime characters are ready for a swipe-right adventure!. Experience real conversations powered by GPT-3.5 or face the sting of rejection with each swipe. Get ready to explore a unique blend of anime, tech, and dating simulation!",
            logos: [
                {
                    logoName: "react",
                    logoSrc:"images/logos/react.svg"
                },
                {
                    logoName: "firebase",
                    logoSrc:"images/logos/firebase.svg"
                },
            ]
        },
        {
            name: "Parking Management",
            imgSrc: "images/developing.jpg",
            github: "",
            webUrl: "",
            description: "Coming Soon...",
            logos: [
                {
                    logoName: "react",
                    logoSrc:"images/logos/react.svg"
                },
                {
                    logoName: "django",
                    logoSrc:"images/logos/django.svg"
                },
            ]
        },
        {
            name: "Ecommerce Website",
            imgSrc: "images/developing.jpg",
            github: "",
            webUrl: "",
            description: "Coming Soon...",
            logos: [
                {
                    logoName: "svelte",
                    logoSrc:"images/logos/svelte.svg"
                },
                {
                    logoName: "django",
                    logoSrc:"images/logos/django.svg"
                },
                {
                    logoName: "postgresql",
                    logoSrc:"images/logos/postgresql.svg"
                },
            ]
        },
    ];

    let facts = [
        {
            name: "a Computer Science Undergraduate",
            description:
                "Hello there! I'm a fourth-year Computer Science Undergraduate at Ho Chi Minh University of Technology (Bach Khoa HCM), currently exploring the exciting realms of technology and innovation. With a GPA of 8.7/10, I proudly rank among the top 10% of my fellow students. Join me on this journey where academic excellence and a deep love for computer science converge!.",
        },
        {
            name: "passionate about backend engineering",
            description:
                " I love digging into how digital stuff works and making sure things run smoothly. My passion is all about understanding the core of how things or services function and crafting strong, efficient backend solutions.",
        },
        {
            name: "a Japan enthusiast",
            description:
                " I'm drawn to the captivating culture and eager to learn Japanese for a deeper connection (mainly for buying Anime figure and reading Manga, hehe). こんにちは！私はホアと申します。よろしくお願いします！ ( * ≧∀≦ *)",
        },
    ];

    let works = [
        {
            companyName: "Individual Systems Co.",
            jobTitle: "AI Engineer Intern",
            duration: "06/2023-08/2023",
            responsibility: "Research, improve performance of Legal Chatbot",
            techs: [
                {
                    logoName: "python",
                    logoSrc:"images/logos/python.svg"
                },
                {
                    logoName: "torch",
                    logoSrc:"images/logos/pytorch.svg"
                },
            ]

        }
    ]
</script>

<main class="flex flex-col flex-1 p-4">
    <section id="introPage" class="grid grid-cols-1 lg:grid-cols-2 gap-10 py-8 sm:py-14">
        <div class="flex flex-col lg:justify-center text-center lg:text-left gap-6 md:gap-8 lg:gap-10">
            <h2 class="font-semibold text-4xl sm:text-5xl md:text-6xl">
                Hi! I'm <span class="poppins text-violet-400">Hoa</span> Nguyen
                <br />Wjbu 
                <span class="poppins text-violet-400">Developer</span>
            </h2>
            <p class="text-base sm:text-lg md:text-xl">
                My <span class="text-violet-400"> favorite tech</span> includes React.js, Python (Django or Flask), PostgreSQL or Firebase/Firestore!
            </p>
            <a
                class="blueShadow mx-auto lg:mr-auto lg:ml-0 text-base sm:text-lg md:text-xl poppins relative overflow-hidden px-6 py-3 group rounded-full bg-white text-slate-950 cursor-pointer"
                href="https://www.facebook.com/ngochoa.nguyen.16752/"
                target="_blank"
            >
                <div
                    class="absolute top-0 right-full w-full h-full bg-violet-400 opacity-20 group-hover:translate-x-full z-0 duration-200"
                />
                <h4 class="relative z-9">Get in touch &rarr;</h4>
            </a>
        </div>

        <div class="relative shadow-2xl grid place-items-center">
            <img
                src={"images/profile.png"}
                alt="Profile Avatar"
                class="object-cover z-[2] max-h-[70vh]"
            />
        </div>

    </section>

    <section 
        id="working"
        class="py-20 pt-10 lg:pt-16 lg:py-32 flex flex-col gap-16 sm:gap-20 md:gap-24 relative"
    >
    <div
        class="flex flex-col gap-2 text-center relative before:absolute before:top-0 before:left-0 before:w-2/3 before:h-1.5 before:bg-violet-700 after:absolute after:bottom-0 after:right-0 after:w-2/3 after:h-1.5 after:bg-violet-700 py-4"
    >
        <h6 class="text-large sm:text-xl md:text-2xl">
            Where I used to work ?
        </h6>
        <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
            <span class="poppins text-violet-400">Working Experiences</span>
        </h3>
    </div>
    <div class="flex flex-col gap-20 w-full mx-auto max-w-[800px]">
        {#each works as work, index}
            <div class="flex gap-6 sm:gap-8">
                <p
                    class="poppins text-4xl sm:text-5xl md:text-6xl text-slate-500 font-semibold"
                >
                    0{index + 1}
                </p>
                <div class="flex flex-col gap-6 sm:gap-8">
                    <h3 class="text-2xl sm:text-3xl md:text-5xl">
                        {work.companyName}
                    </h3>
                    <h3 class="text-l sm:text-xl md:text-2xl">
                        {work.jobTitle} ({work.duration})
                    </h3>
                    <div class="flex space-x-8">
                        <h3 class="text-m sm:text-l md:text-xl">
                            Technology Used:
                        </h3>
                        {#each work.techs as tech}
                            <img src={tech.logoSrc} alt={tech.logoName} width="25">
                        {/each}
                    </div>
                </div>
            </div>
        {/each}
    </div>
    </section>

    <section class="py-20 lg:py-32 flex flex-col gap-24" id="projects">
        <div class="flex flex-col gap-2 text-center">
            <h6 class="text-large sm:text-xl md:text-2xl">
                A few of my creative endeavors.
            </h6>
            <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
                Curious to <span class="poppins text-violet-400">see</span> my work?
            </h3>
        </div>
        <div class="grid grid-cols-1 lg:grid-cols-3 gap-12 lg:gap-10">
            {#each steps as step}
                <Step step={step}/>
            {/each}
        </div>
    </section>

    <section 
        id="about"
        class="py-20 pt-10 lg:pt-16 lg:py-32 flex flex-col gap-16 sm:gap-20 md:gap-24 relative"
    >
    <div
    class="flex flex-col gap-2 text-center relative before:absolute before:top-0 before:left-0 before:w-2/3 before:h-1.5 before:bg-violet-700 after:absolute after:bottom-0 after:right-0 after:w-2/3 after:h-1.5 after:bg-violet-700 py-4"
    >
        <h6 class="text-large sm:text-xl md:text-2xl">
            Want to know more?
        </h6>
        <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
            A bit <span class="poppins text-violet-400">about</span> me.
        </h3>
    </div>
    <p class="mx-auto poppins font-semibold text-lg sm:text-xl md:text-2xl">
        I am . . .
    </p>
    <div class="flex flex-col gap-20 w-full mx-auto max-w-[800px]">
        {#each facts as fact, index}
            <div class="flex gap-6 sm:gap-8">
                <p
                    class="poppins text-4xl sm:text-5xl md:text-6xl text-slate-500 font-semibold"
                >
                    0{index + 1}
                </p>
                <div class="flex flex-col gap-6 sm:gap-8">
                    <h3 class="text-2xl sm:text-3xl md:text-5xl">
                        {fact.name}
                    </h3>
                    <p>{fact.description}</p>
                </div>
            </div>
        {/each}
    </div>
    </section>
</main>