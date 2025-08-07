<script>
  let {
    custName = 'Customer Name',
    custTitle = 'Verified Graduate',
    custAvatar = 'image-daniel.jpg',
    imgBrColor = 'white',
    highlight = 'Customer testimonial highlight',
    testimonial = 'Testimonial body content',
    cardColor = 'purple-dk',
    cardText = 'white-li',
    accentImg = ""
  } = $props()
  
  const bgColorMap = {
    'purple-li': 'bg-purple-li',
    'purple-md': 'bg-purple-md',
    'purple-dk': 'bg-purple-dk',
    'grey-dk': 'bg-grey-dk',
    'white-li': 'bg-white',
    'black-theme': 'bg-black-theme'
  }
  const txtColorMap = {
    'grey-xli': 'text-grey-xli',
    'grey-md': 'text-grey-md',
    'grey-dk': 'text-grey-dk',
    'white-li': 'text-white',
  }
  
  const bdrColorMap = {
    'purple': 'border-purple-md',
    'white':  'border-grey-li',
    'grey':   'border-grey-dk',
  }

</script>

<style>


</style>


<div class="
          min-h-[275px] min-w-0 w-full max-w-full sm:min-w-[250px] sm:max-w-[545px]
          {bgColorMap[cardColor]} {txtColorMap[cardText]}
          rounded-xl shadow-[24px_24px_24px_rgba(0,0,0,0.20)] p-7.5
          text-left relative z-10 h-full"
>
  <!--  TODO: Find way to align image with the two lines of text properly -->
  
  <section class="flex flex-row align-center items-center text-left pb-4">
    <!--    TODO: Figure out image border w/ rounded edges-->
    <img
        src="{import.meta.env.BASE_URL + custAvatar}"
        alt="CustImg"
        class="rounded-full object-cover h-[30px] w-[30px] border-2 {bdrColorMap[imgBrColor]} mr-3 "
    >
    <div>
      <p class="text-sm font-medium">{custName}</p>
      <p class="text-xs font-extralight">{custTitle}</p>
    </div>
  </section>
  <section class="relative text-xl text-left z-10 pb-4 font-bold">
    {highlight}
  </section>
  <article class="text-[13px] font-normal ">
    {testimonial}
  </article>
  {#if accentImg !== ""}
    <img
        src="{import.meta.env.BASE_URL + 'bg-pattern-quotation.svg'}"
        alt="QuoteAccent"
        class="absolute top-0 right-6 md:right-8 z-0"
    />
  {/if}
</div>

