<script lang='ts'>
	import ContentContainer from '$lib/components/content-container.svelte';
	import TextImageContainer from '$lib/components/text-image-container.svelte';
	import Card from '$lib/components/Card.svelte';


	let showScrollArrow = true;
	let showScrollDownArrow = true;

</script>

<svelte:window on:wheel={() => showScrollDownArrow=false} />
<svelte:head>
	<title>Alisa - Dance Professionally</title>
</svelte:head>

<!-- Huuuge landing image with my name on it , supposed to have the "Hello there"-effect-->
<section class='helloThere'>
	<ContentContainer>
		<div class='nameContainer'>
			<div class='name'>
				<h1>
					Alisa <br />Mićunović
				</h1>
			</div>
		</div>
	</ContentContainer>
	<!-- Down arrow to show user that there is more content below -->
	<div class='arrowContainer' class:hidden={!showScrollDownArrow}>
		<svg xmlns='http://www.w3.org/2000/svg' class='icon' viewBox='0 0 512 512'>
			<path fill='none' stroke='#ffffff' stroke-linecap='round' stroke-linejoin='round' stroke-width='48'
						d='M112 184l144 144 144-144' />
		</svg>
	</div>
</section>

<section class='bioSection'>
	<TextImageContainer
		title='Who am I?'
		text='A dancer, weaving the tapestry of movement and emotion. From the vibrant streets of Belgrade to the graceful stages of Munich, I explore the depths of my identity through contemporary dance. With each leap, twist, and turn, I embrace the power of self-expression, finding my truest self in the rhythm of my body. Dance is my language, and with every performance, I reveal a piece of my soul to the world.'
		image='/assets/Alisa2.webp'
	/>
	<TextImageContainer
		title='Why is my dance different?'
		text='It stems from a relentless pursuit of individuality and creative exploration. In a sea of diverse movement styles, my dance stands out for its daring and unconventional approach. I embrace the freedom to break boundaries, challenge norms, and push the limits of what is possible. My choreography reflects my fearless spirit, blending fluidity with unexpected moments of tension and raw emotion. I strive to create a dialogue between the body and the soul, leaving audiences mesmerized by the sheer audacity and authenticity of my performances. My dance is a testament to the power of artistic expression and a constant reminder that true innovation comes from embracing the unfamiliar.'
		image='/assets/Alisa3.webp'
	/>
	<TextImageContainer
		title='Unleashing Boundless Creativity: The Artistic Journey Continues'
		text='In the ever-evolving world of contemporary dance, "Unleashing Boundless Creativity: The Artistic Journey Continues" encapsulates the relentless pursuit of artistic growth and exploration. With each step, leap, and expression, I embark on a never-ending quest to delve deeper into the realms of creativity. Guided by passion and fueled by inspiration, my artistic journey knows no bounds. It is a testament to the infinite possibilities that dance offers, as I constantly challenge myself to stretch beyond comfort zones and embrace new artistic territories. As I continue on this path, I eagerly invite the audience to join me on a captivating voyage of innovation, self-discovery, and the unending pursuit of artistic excellence.'
	/>
</section>
<section style='margin-top: 100px'>
	<h2>
		My Work
	</h2>
	{#if showScrollArrow}
		<div class='scrollArrowContainer'>
			<svg xmlns='http://www.w3.org/2000/svg' class='icon' viewBox='0 0 512 512'>
				<path fill='none' stroke='currentColor' stroke-linecap='round' stroke-linejoin='round' stroke-width='48'
							d='M184 112l144 144-144 144' />
			</svg>
		</div>
	{/if}

	<ContentContainer>
		<div class='scrollContainer' on:scrollend={() => showScrollArrow = false}>
			<div class='myWorkContainer'>
				<Card
					heading='Temptation'
					text="I am thrilled to present to you a captivating contemporary dance piece that delves into the profound concept of temptation. Through this choreography, I aim to explore the intricate dynamics between desire and restraint, offering a thought-provoking experience for the audience.

In this performance, a single dancer takes center stage, their body becoming a vessel for the expression of internal conflicts and human vulnerabilities. Every movement is carefully crafted to reflect the multifaceted nature of temptation, showcasing the dancer's agility, strength, and emotional depth.

At the heart of this choreography lies a symbolic prop—an apple. The apple, often associated with temptation in various narratives, becomes a focal point, representing the allure of forbidden desires. The dancer's interaction with the apple takes on a mesmerizing quality, as they engage in a delicate dance of attraction, hesitation, and struggle.

Through fluid and seamless movements, the dancer explores the push and pull of temptation, embodying the eternal human predicament of giving in or resisting. The choreography intertwines moments of seduction and vulnerability, highlighting the complexities of the human experience.

The performance invites the audience to embark on a journey of self-reflection, as they witness the universal struggle with temptation unfold before their eyes. The choreography aims to spark conversations and introspection, provoking questions about the choices we make and the consequences they hold.

Overall, this contemporary dance piece on temptation seeks to captivate and move the audience, evoking a range of emotions and leaving them with a lingering sense of contemplation. It is my hope that through this choreography, we can shed light on the profound complexities of human nature and the eternal battle between succumbing to temptation or finding the strength to resist its tantalizing allure."
					image='/assets/PB256642.webp'
				/>
				<Card
					heading='Journey'
					text='Step into the enigmatic realm of a contemporary dance performance that beckons you to explore the depths of a journey with no return. In this captivating choreography, the true meaning lies shrouded in mystery, inviting the audience to unravel their own interpretations and embark on a personal voyage of introspection.

Mariella and Victoria grace the stage, holding a slender thread that becomes the emblematic conduit of their irreversible odyssey. With fluid movements and poetic gestures, they navigate the intricacies of existence, each step resonating with a profound sense of purpose and the ceaseless progression of time.

The thread, a symbolic lifeline, hints at the profound significance of the journey undertaken. Its ethereal nature leaves room for speculation, inviting contemplation about the nature of our own lives and the uncharted paths we traverse. As the dancer weaves and twines the thread through their movements, the true essence of this enigmatic expedition becomes an enigma to be deciphered by each individual spectator.

Through mesmerizing choreography, the performance evokes an array of emotions and sparks a sense of curiosity, encouraging the audience to embrace their own interpretations. The dance unveils glimpses of joy, vulnerability, longing, and transformation, leaving fragments of meaning scattered along the intangible pathway.

As the performance reaches its climax, the dancer arrives at a threshold—a moment of profound significance that tantalizingly lingers in the air. The true meaning of the journey remains concealed, allowing the audience to weave their own narratives, weaving personal experiences, aspirations, and desires into the rich tapestry of the performance.

This contemporary dance piece offers a labyrinth of possibility, where the enigma of the journey with no return captivates the imagination and invites the audience to engage with their own stories. It encourages introspection, challenging each individual to contemplate the inexorable forward motion of life, and to explore the untrodden paths that beckon us all.

Immerse yourself in this mysterious choreography, let the delicate thread of the journey guide your thoughts, and embrace the limitless interpretations that unveil themselves within the depths of your own perception. Embark on this enigmatic voyage of self-discovery and let the secrets of the journey with no return be whispered to you in the recesses of your own imagination.'
					image='/assets/IMG_1127.webp'
				/>
			</div>
		</div>

	</ContentContainer>

</section>

<style lang='scss'>
  @import "static/global.scss";

  section {
    max-width: 100vw;
    position: relative;
  }

  .helloThere {
    position: relative;
  }

  .nameContainer {
    position: relative;
    width: 100%;
    height: 100vh;
    background-size: cover;
    background: url("/assets/Alisa1.webp") no-repeat fixed center;
    overflow: hidden;

    .name {
      font-weight: bold;
      color: $color; /* Adjust the color as needed to ensure visibility */
      margin: 10vw;

    }

    @media screen and (max-width: $mobile) {
      background: url("/assets/Alisa1.webp") no-repeat fixed right;
      background-size: cover;
    }
  }


  .arrowContainer {
    position: absolute;
    transition-duration: 4s;

    width: 100%;
    text-align: center;
    bottom: 2.5vh;
    @media screen and (max-width: $mobile) {
      margin: 2.5vh 0;
    }

    .icon {
      height: 5vh;
    }
  }

  .scrollContainer {
    overflow: auto;
    -ms-overflow-style: none; /* IE and Edge */
    scrollbar-width: none; /* Firefox */
  }

  .myWorkContainer {
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 2rem;
    min-width: min-content;
    width: 100%;
  }

  /* Hide scrollbar for Chrome, Safari and Opera */
  .scrollContainer::-webkit-scrollbar {
    display: none;
  }

  .scrollArrowContainer {
    height: 5vh;
    width: auto;

    position: absolute;
    top: 50%;
    right: 10px;

    background: $background;
    border-radius: 10px;


    .icon {
      height: 100%;
    }
  }

  .hidden {
    opacity: 0;
  }
</style>