<template>
  <div>
    <div class="cont">
        <div class="rw">
          <div class="cl w-12">
            <div class="txt-c p-t-2">
              <h1 class=" txt-300 txt-sz-4">{{name}}</h1>
              <p class="m-b-2 txt-sz-1-6 clr-grey-600 txt-200">{{desc}}</p>
              <div>
                <img src="@/assets/ava.jpg" class="ava m-b-2" width=180 :alt="name" />
              </div>

              <div class="clr-grey-700" id="links">
                <a :href="github" class="txt-sz-2-5 m-1"><i class="mi-github"></i></a>
                <a :href="email"  class="txt-sz-2-5 m-1"><i class="mi-envelope-out"></i></a>
              </div>

            </div>
          </div>
        </div>
    </div>
  </div>
</template>

<script>
import ScrollReveal from 'scrollreveal'

export default {
  name: 'Home',
  data () {
    return {
      name: 'Anton Maisak',
      desc: 'Software develop, photo',
      github: 'https://github.com/avmaisak',
      email: 'mailto:anton@maisak.ru'
    }
  },
  mounted () {
    window.sr = ScrollReveal()
    window.sr.reveal('h1')
    window.sr.reveal('.ava', 200)
    window.sr.reveal('#links a', 300)
  }
}
</script>

<style scoped lang="scss">
img.ava {
  border-radius: 50%;
}
</style>
