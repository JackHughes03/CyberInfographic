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
                <a href="#summary" class="bg-green-900 bg-opacity-50">Coincheck summary</a>
                <a href="#laws" class="bg-purple-900 bg-opacity-50">Legilations/Regulations</a>
                <a href="#response" class="bg-slate-800 bg-opacity-50">Response</a>
            </div>
        </header>
        
        <main class="flex flex-col max-w-7xl mx-auto">            
            <section class="bg-blue-900 w-[95%] mt-10 pb-10 ml-auto z-10">
                
                <img class="absolute z-0 left-0 w-96 mt-20 ml-10 hidden xl:block" src="../assets/images/padlock.png" alt="">
                
                <h2 id="intro">Introduction</h2>
                
                <p>Crypto seems to be an ever evolving currency which is becoming more and more popular. Although this may be good for factors including money <span class="italic underline">growth</span> and <span class="italic underline">trust</span>, just like anything, it comes with its downsides, specifically cybersecurity related issues.</p>
                <p class="mt-6">In this infographic, I will visualise and discuss the 2018 Coincheck attack, arguably one of the <span class="italic underline">biggest Cryptocurrency attacks</span> ever. When this attack occured, laws regarding Cryptocurrency were vague, and served as a good wakeup call for all parties involved. "I will discuss what happened, the legal implications, additional legalities, and global responses. Here is a diagram from cointracker.io (cointracker, 2023) to visualise the biggest Cryptocurrency hacks.</p>
                
                <img src="../assets/images/graph.png" alt="An image to represent largest Cryptocurrency hacks" title="An image to represent largest Cryptocurrency hacks">
            </section>
            
            <section class="bg-green-900 w-[95%] mt-10 pb-10">
                
                <h2 id="summary">Coincheck attack summary</h2>

                <img class="absolute z-0 right-0 w-[500px] mt-20 ml-10 hidden xl:block" src="../assets/images/wallet.png" alt="An image of a wallet" title="An image of a wallet">
                
                <p>Coincheck, a Japanese Cryptocurrency exchange company, was hacked in 2018. hackers managed to steal approximately 523 million NEM tokens, which were valued at around $530 million at the time of the hack.</p>
                <p class="mt-6">The hackers managed to gain access to the companies Cryptocurrency hot wallet through a vulnerability, which allowed them to gain access to the private keys of the wallet.</p>
                <p class="mt-6">A hot wallet is a wallet that stores its assets online. This was easier to hack as the wallet is always online and connected to the internet. This was a huge security flaw in return for quicker access to customers assets.</p>
                <p class="mt-6 text-sm opacity-60">Here is a visualisation from nownodes.io (nownodes, 2022), to show the difference between a hot and cold wallet.</p>
                
                <img src="../assets/images/hotcold.png" alt="Image to show the differences between a hot and cold Cryptocurrency wallet." title="Image to show the differences between a hot and cold Cryptocurrency wallet.">
                
                <div class="py-10 pb-0 px-10 grid grid-cols-2 gap-2">
                    <span class="bg-black text-white px-2 py-2 rounded-md bg-opacity-50 flex items-center justify-center">Attack happened at 3am Japan local time</span>
                    <span class="bg-black text-white px-2 py-2 rounded-md bg-opacity-50 flex items-center justify-center">$518 million was stolen directly from the platform</span>
                    <span class="bg-black text-white px-2 py-2 rounded-md bg-opacity-50 flex items-center justify-center">$22 million was stolen from the customers</span>
                    <span class="bg-black text-white px-2 py-2 rounded-md bg-opacity-50 flex items-center justify-center">Resulted in a 5% drop of bitcoins value</span>
                    <span class="bg-black text-white px-2 py-2 rounded-md bg-opacity-50 flex items-center justify-center">Affected 260,000 users</span>
                    <span class="bg-black text-white px-2 py-2 rounded-md bg-opacity-50 flex items-center justify-center">Coincheck promised to use cash from its own funds to pay back the users</span>
                    <span class="bg-black text-white px-2 py-2 rounded-md bg-opacity-50 flex items-center justify-center">Coincheck did not realise their system was hacked until a few hours after the attack</span>
                    <span class="bg-black text-white px-2 py-2 rounded-md bg-opacity-50 flex items-center justify-center">The hack was a wake up call for the Japanese Government</span>
                </div>
            </section>
            
            <section class="bg-purple-900 w-[95%] mt-10 pb-10 ml-auto">
                <h2 id="laws">Legislations and/or regulations</h2>

                <img class="absolute z-0 left-0 w-96 mt-20 ml-10 hidden xl:block" src="../assets/images/avacado.png" alt="An image of a law avacado" title="An image of a law avacado">
                
                <p>Because this was one of the first biggest Cryptocurrency hacks, it sent shockwaves through the Crypto community, and also law enforcement. Let us see what was a result of this attack:</p>
                
                <ul>
                    <li>Japanese law enforcement launched an investigation into the hack to identify the culprits and try to recover the stolen assets.</li>
                    <li>The Financial Services Agency (FSA) of Japan, increased their oversight of the Cryptocurrency exchanges within Japan. They also conducted security assessments to be sure they comply with regulations.</li>
                    <li>Crypto exchange companies were encouraged to use cold wallet storage so they are not connected to the internet.</li>
                    <li>The hack prompted Japan to implement stricter regulations for Cryptocurrency exchanges. This includes:</li>
                    
                    <ul class="ml-4">
                        <li><span class="font-bold">Licensing requirements</span> - Cryptocurrency exchanges in Japan are required to have a license to operate legally.</li>
                        <li><span class="font-bold">Customer protection</span> - Regulations were put in place to safeguard customer assets to ensure exchanges had adequate security measures.</li>
                        <li><span class="font-bold">Know Your Customers (KYC) And Anti-Money Laundering (AML) Compliance</span> - According to dowjones.com (dowjones, 2023) "KYC references a set of guidelines that financial institutions and businesses follow to verify the identity, suitability, and risks of a current or potential customer.". Exchanges were required to implement these procedures to prevent money laundering and terrorist financing.</li>
                    </ul>
                </ul>
                
                <h3 class="text-white text-xl ml-10 pt-10 font-semibold">Is there any more Japan could have done?</h3>
                <p class="mt-4">Here are some recommendations that Japan could have done to reduce the risk of these hacks happening again:</p>
                
                <ul>
                    <li>Even though Japan introduced a licensing system for Cryptocurrency exchanges, they could have introduced a mandatory security audit for every Cryptocurrency company every 6 months.</li>
                    <li>Japan could warn other countries of the importance of strong Cryptocurrency cybersecurity laws.</li>
                    <li>Japan government could have offered education and awareness campaigns to support customers and regular consumers of the dangers and how to protect themselves.</li>
                </ul>
            </section>
            
            <section class="bg-slate-800 w-[95%] mt-10 pb-10">
                <h2 id="response">Response</h2>

                <img class="absolute z-0 right-0 w-96 mt-20 ml-10 hidden xl:block" src="../assets/images/angry.png" alt="An image of an angry person" title="An image of an angry person">
                
                <h4 class="p-0 pb-10">Private sector</h4>
                <p>Like many, this attack shocked the private sector. Because of this, they began advancing their protection and security in regards to Cryptocurrency.</p>
                
                <ul>
                    <li><span class="font-bold">Enhanced Security Measures - </span>Investigated more advanced security technologies, conducting security audits, and implementing multi-signature wallets, whilst also exploring the advancement of cold wallets.</li>
                    <li><span class="font-bold">Insurance - </span>Some companies who offer exchange services, started to offer insurance as part of their services. This covered protection for their customers assets.</li>
                    <li><span class="font-bold">Collaboration - </span>The Cryptocurrency industry started to come together to work closely to prevent future attacks. Combining skill sets helped them come up with better and more robust ideas.</li>
                    <li><span class="font-bold">Education and Awareness - </span>Because this Coincheck hack serves as a wake-up call for the community, education for customers was upped as a result.</li>
                </ul>
                
                <h4>Individuals</h4>
                <p>Depending on the involvement and their personal experience regarding the Cryptocurrency industry, individuals reactions differed.</p>
                
                <ul>
                    <li><span class="font-bold">Investors - </span>Investors were more careful about investing in Cryptocurrency, as they were worried about the security of their assets and what it could do to their brand.</li>
                    <li><span class="font-bold">Crypto Enthusiasts - </span>Some Crypto enthusiasts were not phased by the hack, and continued to invest in Cryptocurrency. This was the highest probability outcome.</li>
                    <li><span class="font-bold">Crypto Skeptics - </span>Some skeptics used this as an opportunity to criticise Cryptocurrency, and use it as an example of why Cryptocurrency is not a good investment.</li>
                </ul>
            </section>
            
            <section class="bg-red-900 w-[95%] mt-10 pb-10 ml-auto">
                <h2 id="future">Future for cybersecurity with Cryptocurrency</h2>
                
                <img class="absolute z-0 left-0 w-96 -mt-20 ml-10 hidden xl:block" src="../assets/images/crypto.png" alt="An image of a crypto coin" title="An image of a crypto coin">

                <p>So what does this mean for the future of Cryptocurrency across the globe? Well, after evaluating the attack, it seems the only government that took notice of it, was Japan. This attack was arguably one of the biggest Cryptocurrency attacks of all time, and since the attack has occurred, governments still aren't definitely sure what to make out of Cryptocurrency. Even in 2023, Cryptocurrency is not accessible for everyday use. Is this a threat for the government? Would they benefit from working with Cryptocurrency to understand it better to gain control of the harder traceability and different currency? Or do they see it as a threat?</p>
                <p class="mt-4">Western governments in particular, should evaluate in detail the affects of the Coincheck attack and attacks like it, to see what they can do for their own countries. Or will it take another Coincheck attack for governments around the globe to take it seriously?</p>
                <p class="mt-4">These are all questions that will be answered in due time. What is certain is that Cryptocurrency companies in Japan, and the Japanese government, and their new laws, including licensing requirements, customers protection, KYC and AML compliance will be sure they will do their best to make sure nothing like this happens again.</p>
            </section>
            
            <section class="bg-[#ffffff98] w-[95%] mt-10 pb-10 font-serif">
                <h2 class="text-black">References</h2>
                
                <p class="text-black">Nownodes.io (2022) Hot vs cold wallet: How do you store your Crypto?: NOWNodes, News about Nodes | The Official NOWNodes Blog. Available at: <a href="https://nownodes.io/blog/hot-vs-cold-wallet-how-do-you-store-your-crypto/" class="text-blue-800" target="_blank"> https://nownodes.io/blog/hot-vs-cold-wallet-how-do-you-store-your-crypto/ </a> (Accessed: 01 November 2023). </p>
                <p class="text-black mt-4">(2023) Cryptocurrency security guide | cointracker. Available at: <a class="text-blue-800" target="_blank" href="https://www.cointracker.io/blog/cryptocurrency-security-guide">https://www.cointracker.io/blog/cryptocurrency-security-guide</a> (Accessed: 02 November 2023). </p>
                <p class="text-black mt-4">Understanding the steps of a Know your customer process (2023) Dow Jones Professional. Available at: <a href="https://www.dowjones.com/professional/risk/glossary/know-your-customer/#:~:text=KYC%20references%20a%20set%20of,a%20current%20or%20potential%20customer" class="text-blue-800" target="_blank">https://www.dowjones.com/professional/risk/glossary/know-your-customer/#:~:text=KYC%20references%20a%20set%20of,a%20current%20or%20potential%20customer.</a> (Accessed: 02 November 2023). </p>
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
                @apply mt-20 rounded-md max-w-4xl duration-500;
                
                h2 {
                    font-family: 'Exo';
                    @apply text-white font-semibold text-3xl p-10;
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