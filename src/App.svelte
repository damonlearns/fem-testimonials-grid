<script>
  import svelteLogo from './assets/svelte.svg'
  import viteLogo from '/vite.svg'
  import Counter from './lib/Counter.svelte'
  import Testimonial from "./lib/Testimonial.svelte";
</script>


<!--
Grid Layout Pseudo
a a b c
d e e c

Sizing

Avatar Image - 30p x 30p
Name + Img - 30 x 140-150p

-->
<main>
  <div class="card-grid">
    <section class="grid-c-a">
      <Testimonial
          custName="Daniel Clifford"
          custTitle="Verified Graduate"
          highlight="I received a job offer mid-course, and the subjects I learned were current, if not more so, in the company I joined. I honestly feel I got every penny’s worth."
          testimonial="  “ I was an EMT for many years before I joined the bootcamp. I’ve been looking to make a transition and have heard some people who had an amazing experience here. I signed up for the free intro course and found it incredibly fun! I enrolled shortly thereafter. The next 12 weeks was the best - and most grueling - time of my life. Since completing the course, I’ve successfully switched careers, working as a Software Engineer at a VR startup.”"
          accentImg="Render Me Please!"
          imgBrColor="purple"
      />
    </section>
    <section class="grid-c-b">
      <Testimonial
          custName="Jonathan Walters"
          custAvatar="image-jonathan.jpg"
          cardColor="grey-dk"
          highlight="The team was very supportive and kept me motivated"
          testimonial="“ I started as a total newbie with virtually no coding skills. I now work as a mobile engineer
  for a big company. This was one of the best investments I’ve made in myself. ”"
          imgBrColor="grey"
      />
    </section>
    
    <section class="grid-c-d">
      <Testimonial
          custName="Jeanette Harmon"
          custAvatar="image-jeanette.jpg"
          cardColor="white-li"
          cardText="grey-dk"
          highlight="An overall wonderful and rewarding experience"
          testimonial="“ Thank you for the wonderful experience! I now have a job I really enjoy, and make a good living
  while doing something I love. ”"
      />
    </section>
    <section class="grid-c-e">
      <Testimonial
          custName="Patrick Abrams"
          custAvatar="image-patrick.jpg"
          cardColor="black-theme"
          cardText="grey-xli"
          highlight="Awesome teaching support from TAs who did the bootcamp themselves. Getting guidance from them and
  learning from their experiences was easy."
          testimonial="“ The staff seem genuinely concerned about my progress which I find really refreshing. The program
  gave me the confidence necessary to be able to go out in the world and present myself as a capable
  junior developer. The standard is above the rest. You will get the personal attention you need from
  an incredible community of smart and amazing people. ”"
          imgBrColor="purple"
      />
    </section>
    <section class="grid-c-c">
      <Testimonial
          custName="Kira Whittle"
          custAvatar="image-kira.jpg"
          cardColor="white-li"
          cardText="grey-dk"
          highlight="Such a life-changing experience. Highly recommended!"
          testimonial="“ Before joining the bootcamp, I’ve never written a line of code. I needed some structure from
  professionals who can help me learn programming step by step. I was encouraged to enroll by a former
  student of theirs who can only say wonderful things about the program. The entire curriculum and staff
  did not disappoint. They were very hands-on and I never had to wait long for assistance. The agile team
  project, in particular, was outstanding. It took my learning to the next level in a way that no tutorial
  could ever have. In fact, I’ve often referred to it during interviews as an example of my developent
  experience. It certainly helped me land a job as a full-stack developer after receiving multiple offers.
  100% recommend! ”"
      />
    </section>
  
  </div>
</main>

<style>
  
  .card-grid {
    display: grid;
    grid-template-columns: 1fr;
    gap: 2rem;
    max-width: 1200px;
    margin: 0 auto;
    width: 100%;
    box-sizing: border-box;
    grid-template-areas: none;
    grid-template-rows: none;
  }
  
  @media (min-width: 900px) {
    .card-grid {
      grid-template-columns: repeat(4, 1fr);
      grid-template-areas:
      "a a b c"
      "d e e c";
      grid-template-rows: 1fr 1fr;
    }
    
    .grid-c-a {
      grid-area: a;
    }
    
    .grid-c-b {
      grid-area: b;
    }
    
    .grid-c-c {
      grid-area: c;
    }
    
    .grid-c-d {
      grid-area: d;
    }
    
    .grid-c-e {
      grid-area: e;
    }
  }
  
  

</style>
