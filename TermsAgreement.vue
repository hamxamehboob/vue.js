<template>
  <div class="text-sm text-black max-w-[391px]">
    <div class="relative w-full">
      <header class="flex z-0 gap-3 items-center w-full leading-5 underline">
        <img
          src="https://cdn.builder.io/api/v1/image/assets/TEMP/de3ca8453468ed72e72e58f3208eabd26f1fafde?placeholderIfAbsent=true&apiKey=f71265e8a9614b81bd2148178274eb93"
          class="object-contain shrink-0 self-stretch my-auto w-6 aspect-square"
          alt="전체 동의 체크박스"
        />
        <h2 class="self-stretch my-auto w-[348px]">
          알림봇이용약관, 개인정보 수집 및 이용, 프로모션 정보 수신(선택)에 모두 동의합니다.
        </h2>
      </header>

      <AgreementSection
        title="알림봇 이용 약관 동의"
        :show-content="true"
      />

      <AgreementSection
        title="개인정보 수집 및 이용 동의"
        :show-content="true"
      />

      <AgreementSection
        title="프로모션 정보 수신 동의"
        :show-content="false"
      />

      <p class="z-0 mt-5 text-xs text-right">
        문자, 연락처, 이메일에 스마트업 서비스와 관련된 소식을 받아보겠습니다.
      </p>

      <ActionButtons
        @cancel="handleCancel"
        @confirm="handleConfirm"
      />
    </div>
  </div>
</template>

<script>
import AgreementSection from './AgreementSection.vue'
import ActionButtons from './ActionButtons.vue'

export default {
  name: 'TermsAgreement',
  components: {
    AgreementSection,
    ActionButtons
  },
  methods: {
    handleCancel() {
      // Handle cancel action
      console.log('Cancel clicked')
    },
    handleConfirm() {
      // Handle confirm action
      console.log('Confirm clicked')
    }
  }
}
</script>
