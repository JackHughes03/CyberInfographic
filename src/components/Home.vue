<script setup>
    import { ref, onMounted } from 'vue';

    const sections = ref([]);
    const observer = ref(null);

    onMounted(() => {
        sections.value = document.querySelectorAll('section');
        observer.value = new IntersectionObserver(entries => {
            entries.forEach(entry => {
                if (entry.intersectionRatio > 0) {
                    entry.target.classList.add('opacity-100');
                } else {
                    entry.target.classList.remove('opacity-100');
                }
            });
        });

        sections.value.forEach(section => {
            observer.value.observe(section);
        });
    });
</script>

<template>
    <div id="app" class="h-full w-full">
        <header class="w-full h-full">
            <h1 class="text-white text-5xl p-10 font-[cabinsketch]">
                <span>Cryptocurrency Coincheck Attack:</span><br> 
                <span class="text-xl ml-1 opacity-70 font-light">Exploring the Notorious Coincheck Crypto attack and Responses from all around</span>
            </h1>
            
            <div class="inline-flex flex-col p-10 gap-2 absolute bottom-0 introbuttons">
                <a href="#intro" class="bg-blue-900 bg-opacity-50">Introduction</a>
                <a href="#pipeline" class="bg-green-900 bg-opacity-50">Coincheck summary</a>
                <a href="#polynetwork" class="bg-purple-900 bg-opacity-50">Legilations/Regulations</a>
                <a href="#laws" class="bg-slate-800 bg-opacity-50">Response</a>
            </div>
        </header>
        
        <main class="flex flex-col max-w-7xl mx-auto">            
            <section class="bg-blue-900 w-[95%] mt-10 pb-10 ml-auto">
                <h2 id="intro">Introduction</h2>
                
                <p>Crypto seems to be an ever evolving currency which is becoming more and more popular. Although this may be good for factors including money growth and trust, just like anything, it comes with its downsides, specifically cyber issues...</p>
                <p class="mt-6">In this infographic, I will visualise and discuss the 2018 Coincheck attack, arguably one of the biggest cryptocurrency attacks ever. I will show what happened, aswell as global responses. Here is a diagram from cointracker.io (cointracker, 2023) to visualise the biggest cryptocurrency hacks.</p>

                <img src="../assets/images/graph.png" alt="Image to represent largest cryptocurrency hacks" title="Image to represent largest cryptocurrency hacks">
            </section>
            
            <section class="bg-green-900 w-[95%] mt-10 pb-10">
                <h2>Coincheck attack summary</h2>
                
                <p>Coincheck, a Japanese cryptocurrency exchance company, was hacked in 2018. They managed to steal approximately 523 million NEM tokens, which were valued at around $530 million at the time of the hack.</p>
                <p class="mt-6">The hackers managed to gain access to the companies cryptocurrency hot wallet through a vulnerability, which alloewed them to gain access to the private keys of the wallet.</p>
                <p class="mt-6">A hot wallet is a wallet that stores its assets online. This was easier to hack as the wallet is always online. Here is an image from nownodes.io (nownodes, 2022), to show the difference between a hot and cold wallet.</p>

                <img src="../assets/images/hotcold.png" alt="Image to show the differences between a hot and cold cryptocurrency wallet." title="Image to show the differences between a hot and cold cryptocurrency wallet.">
            </section>
            
            <section class="bg-purple-900 w-[95%] mt-10 pb-10 ml-auto">
                <h2 id="laws">Legislations and/or regulations</h2>
                
                <p>Because this was one of the first biggest cryptocurrency hacks, it sent shockwaves through the crypto community, and also law enforcement. Lets see what was a result of this attack:</p>
                
                <ul>
                    <li>Japanese law enforcement launched an investigation into the hack to identify the culprits and try to recover the stolen assets.</li>
                    <li>The Financial Services Agency (FSA) of Japan, increased their oversight of the cryptocurrency exchanges within Japan. They also conducted security assessments to be sure they comply with regulations.</li>
                    <li>Exchanges were encouraged to use cold wallet storage, which is an offline way to store funds.</li>
                    <li>The hack prompted Japan to implement stricter regulations for cryptocurrency exchanges. This includes:</li>

                    <ul class="ml-4">
                        <li><span class="font-bold">Licensing requirements</span> - Cryptocurrency exchanges in Japan are required to have a license to operate legally.</li>
                        <li><span class="font-bold">Customer protection</span> - Regulations were put in place to safeguard customer assets to ensure exchanges had adequate security measures.</li>
                        <li><span class="font-bold">Know Your Customers (KYC) and Anti-Money Laundering (AML) Compliance</span> - Exchanges were requires to implement these procedures to prevent money laundering and terrorist financing.</li>
                    </ul>
                </ul>
            </section>
            
            <section class="bg-slate-800 w-[95%] mt-10 pb-10">
                <h2>Response</h2>

                <h4 class="p-0 pb-10">Private sector</h4>
                <p>Like many, this attack shocked the private sector. Because of this, they began advancing their protection and security in regards to cryptocurrency.</p>

                <ul>
                    <li><span class="font-bold">Enchanced Security Measures - </span>Investigated more advanced security technologies, conducting security audits, and implementing multi-signature wallets, whilst also exploring the advancement of cold wallets.</li>
                    <li><span class="font-bold">Insurance - </span>Some companies who offer exchange services, started to offer insurance as part of their services. This covered protection for their customers assets.</li>
                    <li><span class="font-bold">Collaboration - </span>The cryptocurrency industry started to come together to work closely to prevent future attacks. Combining skill sets helped them come up with better and more robust ideas.</li>
                    <li><span class="font-bold">Education and Awareness - </span>Because this Coincheck hack serves as a wake-up call for the community, education for customers was upped as a result.</li>
                </ul>

                <h4>Individuals</h4>
                <p>Depending on the involvement and their personal experience regarding the cryptocurrency industry, individuals reacted differently.</p>

                <ul>
                    <li><span class="font-bold">Investors - </span>Investors were more careful about investing in cryptocurrency, as they were worried about the security of their assets and what it could do to their brand.</li>
                    <li><span class="font-bold">Crypto Enthusiasts - </span>Some crypto enthusiasts were not phased by the hack, and continued to invest in cryptocurrency. This was the highest probability outcome.</li>
                    <li><span class="font-bold">Crypto Skeptics - </span>Some skeptics used this as an opportunity to criticise cryptocurrency, and use it as an example of why cryptocurrency is not a good investment.</li>
                </ul>
            </section>

            <section class="bg-[#ffffff98] w-[95%] mt-10 pb-10 ml-auto font-serif">
                <h2 class="text-black">References</h2>

                <p class="text-black">Nownodes.io (2022) Hot vs cold wallet: How do you store your crypto?: NOWNodes, News about Nodes | The Official NOWNodes Blog. Available at: <a href="https://nownodes.io/blog/hot-vs-cold-wallet-how-do-you-store-your-crypto/" class="text-blue-800" target="_blank"> https://nownodes.io/blog/hot-vs-cold-wallet-how-do-you-store-your-crypto/ </a> (Accessed: 01 November 2023). </p>
            </section>
        </main>

        <footer class="text-white text-center py-4 text-sm mt-10">Coded using 
            <a href="https://vuejs.org/" target="_blank">VueJS</a>, 
            <a href="https://tailwindcss.com/" target="_blank">Tailwind</a>, and 
            <a href="https://sass-lang.com/" target="_blank">sass</a> by Jack Hughes 2023
        </footer>
    </div>
</template>

<style lang="postcss">
    @font-face {
        font-family: 'Exo';
        src: url('../assets/fonts/Exo2.ttf');
    }
    
    @font-face {
        font-family: 'CabinSketch';
        src: url('../assets/fonts/CabinSketch.ttf');
    }
    
    html {
        scroll-behavior: smooth;
        
        header {
            background-image: url('../assets/images/computer.webp');
            background-size: cover;
            background-position: center;
            background-repeat: no-repeat;
            font-family: 'Exo';
            
            .introbuttons {
                a {
                    @apply text-white cursor-pointer text-left px-4 py-4 rounded backdrop-blur-sm duration-300;
                    
                    &:hover {
                        @apply bg-opacity-100;
                    }
                }
            }
        }
        
        main {            
            section {
                @apply mt-20 rounded-md max-w-4xl opacity-0 duration-500;
                
                h2 {
                    font-family: 'Exo';
                    @apply text-white font-semibold text-3xl p-10;
                }
                
                h3 {
                    @apply text-white pb-10 text-xl ml-10 pt-2 font-semibold underline;
                }

                h4 {
                    @apply text-white pb-8 text-base ml-10 pt-10 font-semibold underline;
                }
                
                p {
                    @apply text-white text-base px-10 -mt-6;
                }
                
                img {
                    @apply w-[89%] max-w-4xl mt-4 mx-auto;
                }
                
                ul {
                    @apply text-white ml-20 mt-4 list-disc pr-10;
                }
            }
        }

        footer {
            a {
                @apply underline text-blue-200;
            }
        }
    }
</style>