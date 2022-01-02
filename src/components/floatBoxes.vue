<template>
    <section id="us">
      <h1>Honrados de compartirle nuestra esencia.</h1>
      <div class="container">
        <div class="floted up">
          <img :src="picture1" class="floatImages"/>
        </div>
        <div class="floted fText down">
          <h2>Sed ut perspiciatis unde omnis iste natus error sit</h2>
          <p>Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsa quae ab illo inventore veritatis et quasi architecto beatae vitae dicta sunt explicabo. Nemo enim ipsam voluptatem quia voluptas sit aspernatur aut odit aut fugit, sed quia consequuntur Nemo enim ipsam voluptatem quia voluptas sit aspernatur aut odit aut fugit, sed quia consequuntur Nemo enim ipsam voluptatem quia voluptas sit aspernatur aut odit aut fugit, sed quia consequuntur</p>
        </div>
      </div>
      <div class="container">
        <div class="floted fText up">
          <h2>Sed ut perspiciatis unde omnis iste natus error sit</h2>
          <p>Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsa quae ab illo inventore veritatis et quasi architecto beatae vitae dicta sunt explicabo. Nemo enim ipsam voluptatem quia voluptas sit aspernatur aut odit aut fugit, sed quia consequuntur Nemo enim ipsam voluptatem quia voluptas sit aspernatur aut odit aut fugit, sed quia consequuntur Nemo enim ipsam voluptatem quia voluptas sit aspernatur aut odit aut fugit, sed quia consequuntur</p>
        </div>
        <div class="floted down">
          <img :src="picture2" class="floatImages"/>
        </div>
      </div>
    </section>
</template>

<script>
import picture1 from "../assets/_DSC5166.jpg";
import picture2 from "../assets/_DSC5129.jpg";

export default {
  name: 'FloatBoxes',
  data() {
    return {
      picture1,
      picture2
    };
  },
}
</script>

<style scoped>
@import "../styleComponents/floatBoxes.scss";
</style>
