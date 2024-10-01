<script>
    import Step from "./Step.svelte";
    
    let steps = [
        {
            name: "Ecommerce Shop",
            icon: "fa-solid fa-cart-shopping",
            image: "images/eshop.PNG", // Ensure this path matches your public directory
        },
        {
            name: "HR Management System",
            icon: "fa-solid fa-user-tie",
            image: "images/received_955288499094961.jpeg",
        },
        {
            name: "Student Management System",
            icon: "fa-solid fa-graduation-cap",
            image: "images/Messenger_creation_1307593076608699.jpeg",
        },
    ];

    let benefits = [
        {
            metric: "10x",
            name: "What Is My Passion",
            description: "I'm passionate about graphic design and on a journey to learn more about the art of visual storytelling. I believe that good design can make the world a more beautiful, functional, and meaningful place.",
        },
        {
            name: "The Interest",
            description: "My interest in design started when I realized how much visual elements can influence emotions and convey messages without words. Since then, I've been diving into design principles, experimenting with different styles, and exploring new tools to enhance my skills.",
        },
        {
            name: "My Goal",
            description: "Is to become a professional graphic designer, working on projects that not only look good but also solve real problems and resonate with audiences.",
        },
    ];
</script>

<main class="flex flex-col flex-1 p-4">
    <section id="introPage" class="grid grid-cols-1 lg:grid-cols-2 gap-10 py-8 sm:py-14">
        <div class="flex flex-col lg:justify-center text-center lg:text-left gap-6 md:gap-8 lg:gap-10">
            <h2 class="font-semibold text-4xl sm:text-5xl md:text-6xl">
                Hello I'm <span class="poppins text-orange-400">Abie</span> Pajaro
                <br /> From BSCS 3C
            </h2>
            <p class="text-base sm:text-lg md:text-xl">
                Fueling Curiosity <span> Empowering Futures at</span>
                <span class="text-orange-400">Gordon College</span>
            </p>
        </div>
        <div class="relative grid place-items-center">
            <img
                src="/images/abie.png"
                alt="Zetane Engine"
                class="object-cover z-[2] max-h-[70vh]"
            />
        </div>
    </section>

    <section class="py-20 lg:py-32 flex flex-col gap-24" id="projects">
        <div class="flex flex-col gap-2 text-center">
            <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
                My College Year Projects
            </h3>
        </div>

        <div>
            {#each steps as step}
                <Step step={step}>
                    <p>{step.name}</p>
                </Step>
            {/each}
        </div>
    </section>

    <section id="about" class="py-20 pt-10 lg:pt-16 lg:py-32 flex flex-col gap-16 sm:gap-20 md:gap-24 relative">
        <div class="flex flex-col gap-2 text-center relative before:absolute before:top-0 before:left-0 before:w-2/3 before:h-1.5 before:bg-orange-700 after:absolute after:bottom-0 after:right-0 after:w-2/3 after:h-1.5 after:bg-orange-700 py-4">
            <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
                <span class="poppins text-orange-400">About</span> Me
            </h3>
        </div>
        <div class="flex flex-col gap-20 w-full mx-auto max-w-[800px]">
            {#each benefits as benefit, index}
                <div class="flex gap-6 sm:gap-8">
                    <p class="poppins text-4xl sm:text-5xl md:text-6xl text-amber-50 font-semibold">
                        0{index + 1}
                    </p>
                    <div class="flex flex-col gap-6 sm:gap-8">
                        <h3 class="text-2xl sm:text-3xl md:text-5xl">
                            {benefit.name}
                        </h3>
                        <p>{benefit.description}</p>
                    </div>
                </div>
            {/each}
        </div>
    </section>
</main>