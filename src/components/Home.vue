<script setup>
    import { ref, onMounted } from 'vue';
</script>

<template>
    <div id="app" class="h-full w-full">
        <header class="w-full h-full">
            <h1 class="text-white text-5xl max-w-[1100px] p-10 font-[cabinsketch]">
                <span>Cryptocurrency Underworld Unveiled:</span><br> 
                <span class="text-xl ml-1 opacity-70 font-light">Exploring Notorious Crypto Crimes and Global Responses</span>
            </h1>
            
            <div class="flex flex-wrap p-10 gap-2 max-w-4xl introbuttons">
                <a href="#intro">Introduction</a>
                <a href="#pipeline">Colonial Pipeline ransomware</a>
                <a href="#polynetwork">Poly Network</a>
                <a href="#laws">Legislations and/or regulations</a>
                <!-- <button>The Culprits</button>
                    <button>The Legal Response</button>
                    <button>Global Response</button>
                    <button>Protecting Your Assets</button>
                    <button>Prevention and Awareness</button> 
                -->
                <a>Conclusion</a> 
            </div>
        </header>
        
        <main>
            <img class="float-right w-96 mr-8 mt-8" src="../assets/images/piechart.png" alt="">
            
            <section class="mt-0">
                <h2 id="intro">Introduction</h2>
                
                <p>Crypto seems to be an ever evolving currency which is becoming more and more popular. Although this may be good for factors including money growth and trust, just like anything, it comes with its downsides, specifically cyber issues...</p>
                <p class="mt-6">In this infographic, I will visualise and discuss the current and potential crypto crimes and legal responses. Here is a diagram to visualise the percentage of how cyber attacks happen in crypto currency.</p>
            </section>
            
            <section>
                <h2>Crypto Cyber Incidents</h2>
                
                <h3 id="pipeline">Colonial Pipeline ransomware</h3>
                <p>Now due to the harder traceability of crypto currency transactions, a lot of hackers demand payment through some sort of crypto currency.</p>
                <p class="mt-6">In may 2021, the Colonial Pipeline, a major fuel pipeline in the US, was hit by a ransomware attack that forced it to shutdown. The hackers demanded a payment of 4.4 million USD through Bitcoin in exchange for the decryption key to unlock the pipeline's systems.</p>
                <p class="mt-6">The pipeline was shut down for 6 days, resulting in a fuel shortage in the US. The pipeline's CEO, Joseph Blount, said that he authorised the payment because he was unsure how long the shutdown would last and did not want to risk the public's safety. Although the company authorised the payment, the FBI conducted an investigation into what happened, working closely with various cybersecurity experts and private partners to trace the attackers origin.</p>
                <p class="mt-6">The FBI was able to recover some of the stolen funds.</p>
                
                <img class="mt-10" src="../assets/images/pipeline.webp" alt="">
                
                <h3 id="polynetwork" class="mt-10">Poly network</h3>
                <p>In August 2021, hackers stole cryptocurrencies worth over 600 million USD in the form of crypto from Poly Network, which is a finance platform. The hacker later on said they did it 'for fun', although significant damage was done to not only Poly Network's reputation, but their financial assets, resulting in money freezes.</p>
                <p class="mt-6">The hacker returned the money, but the incident still raised questions about the security of crypto currency. Below is a visual representation of the hacker recieving the money.</p>
                <p class="mt-6"></p>
                
                <img src="../assets/images/polynetwork.png" alt="">
            </section>
            
            <section>
                <h2 id="laws">Legislations and/or regulations</h2>
                
                <h3>UK</h3>
                <p>Currently, the UK do not have any specific laws and regulations for crypto currency, however, they are looking at implementing some to regulate the growing crypto market.</p>
                <p class="mt-0">Here are some recommendations:</p>
                
                <ul>
                    <li>Licenses and Registration for Crypto businesses - This will help the authorities to oversee what is going on more easier.</li>
                    <li>Anti-Money Laundering (AML) and Know Your Customer (KYC) - This will help to prevent money laundering and other illegal activities.</li>
                    <li>Consumer Protection - Crypto currency scams are huge right now and this needs to be regulated. This will help to protect consumers from said scams.</li>
                    <li>Market Integrity - The crypto market can be influenced by people with a big following, such as Elon Musk. Perhaps some laws regarding these activities need to be put in place.</li>
                </ul>
                
                <h3 class="mt-10">USA</h3>
                <p>The US have a few laws and regulations in place for crypto currency, however, they are not as strict as they could be. Here are some of the laws and regulations in place:</p>
                
                <ul>
                    <li>The Arizona State Senate introduced a bill that would amend the definition of legal tender to include Bitcoin.</li>
                    <li>Iowa introduced a bill that would prohibit the state from accepting payment in the form of cryptocurrencies.</li>
                </ul>
                
                <p class="mt-8">Below is a quick representational diagram map to showcase cryptocurrency regulations in each country.</p>
                
                <img src="../assets/images/crypto-regulations.jpg" alt="">
            </section>
            
            <section>
                <h2>Global Response</h2>

                <h3>Cryptocurrency cybersecurity response</h3>
                
                <h4 class="pt-0">Government</h4>
                <p>As a whole, governments around the world are responding to the current state of cybersecurity in cryptocurrency like they would with anything, although because this is a modern and technical situation, they need to respond slightly differently. Lets take a look at what governments around the world are doing:</p>

                <ul>
                    <li>Some governments like the United Kingdom, Japan, South Korea, Malta, Singapore, United States, and Australia have implemented licensing requirements for cryptocurrency exchanges, or were in the process of considering this.</li>
                    <li>Some governments have been cooperating at international level to share information and combat crimes regarding cryptocurrency.</li>
                    <li>Governments around the world have introduced or supported the idea of public awareness campaigns to educate citizens about the risks of associating with cryptocurrencies.</li>
                </ul>

                <h4>Private sector</h4>
                <p>The private sector has also been responding to the current state of cybersecurity in cryptocurrency. The private sector most likely contains talented people with good skill sets, so it would make sense to engage in some sort of response. Here are some examples:</p>

                <ul>
                    <li>Numerous cybersecurity companies have started to address the needs for cybersecurity within the cryptocurrency industry. They offer services like wallet security, security audits, penetration testing, and incident response services.</li>
                    <li>Companies have started creating Multi-signature and hardware wallets to provide enhanced and better security.</li>
                    <li>The private sector have also started to develop insurance to protect the assets that people invest in.</li>
                </ul>

                <h4>Individuals</h4>
                <p>Because people who dabble in cryptocurrency are usually doing it by themselves, hoping that the price of their cryptocurrency goes up, this means they're more vunerable and need to be more aware of what is going on. They can only do as much as the companies who help protect them. Lets see how they responded to it:</p>

                <ul>
                    <li>A 74 year old male named Naum Lantsman got scammed out of 340 million USD worth of cryptocurrency. In an interview, his daughter said 'I lost 100% of my family's liquidity'.</li>
                    <li>In a report by the FTC, it is said that in 2021, 680 million USD worth of cryptocurrencies was stolen by fraud.</li>
                </ul>
            </section>
            
            <section>
                <h2>Prevention and Awareness</h2>
            </section>
            
            <section>
                <h2>Conclusion</h2>
            </section>
        </main>
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
                    @apply text-white cursor-pointer text-left px-4 bg-[#ffffff25] py-2 rounded backdrop-blur-sm duration-300;
                    
                    &:hover {
                        @apply bg-[#333333];
                    }
                }
            }
        }
        
        main {
            @apply  max-w-4xl mx-auto;
            
            section {
                @apply mt-20;
                
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
    }
</style>


<!-- Naum Lantsman: https://www.npr.org/2023/06/25/1180256165/crypto-scam-senior-victims-spirebit -->