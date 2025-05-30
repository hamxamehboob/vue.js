<template>
  <div class="flex relative z-0 gap-6 items-start mt-5 w-full text-white whitespace-nowrap">
    <button
      class="flex z-0 shrink-0 my-auto h-12 bg-neutral-400 w-[180px] items-center justify-center"
      @click="$emit('cancel')"
    >
      취소
    </button>
    <button
      class="flex z-0 shrink-0 my-auto h-12 bg-orange-500 w-[180px] items-center justify-center"
      @click="$emit('confirm')"
    >
      확인
    </button>
  </div>
</template>

<script>
export default {
  name: 'ActionButtons',
  emits: ['cancel', 'confirm']
}
</script>
