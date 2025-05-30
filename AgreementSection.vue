<template>
  <section>
    <div class="flex z-0 gap-3 items-center mt-5 w-full leading-loose underline">
      <img
        src="https://cdn.builder.io/api/v1/image/assets/TEMP/de3ca8453468ed72e72e58f3208eabd26f1fafde?placeholderIfAbsent=true&apiKey=f71265e8a9614b81bd2148178274eb93"
        class="object-contain shrink-0 self-stretch my-auto w-6 aspect-square"
        :alt="`${title} 체크박스`"
      />
      <h3 class="self-stretch my-auto w-[348px]">
        {{ title }}
      </h3>
    </div>
    <TextContentArea v-if="showContent" />
  </section>
</template>

<script>
import TextContentArea from './TextContentArea.vue'

export default {
  name: 'AgreementSection',
  components: {
    TextContentArea
  },
  props: {
    title: {
      type: String,
      required: true
    },
    showContent: {
      type: Boolean,
      default: true
    }
  }
}
</script>
