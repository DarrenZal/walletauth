<script lang="ts">
  import { appName } from '$lib/app-info'
  import Connect from '$components/auth/connect/Connect.svelte'
</script>

<div
  class="min-h-[calc(100vh-96px)] flex flex-col items-start justify-center max-w-[700px] m-auto gap-6 pb-5 text-sm"
>
  <h1 class="text-xl">Welcome to {appName}</h1>

  <div class="max-w-[590px]">
   <!--  <p class="mb-5">
      The ODD SDK is a true local-first edge computing stack. Effortlessly
      give your users:
    </p>

    <ul class="mb-6 pl-6 list-disc">
      <li>
        <span class="font-bold">modern, passwordless accounts</span>
        , without a complex and costly cloud-native back-end
      </li>
      <li>
        <span class="font-bold">user-controlled data</span>
        , secured by default with our encrypted-at-rest file storage protocol
      </li>
      <li>
        <span class="font-bold">local-first functionality</span>
        , including the ability to work offline and collaborate across multiple devices
      </li>
    </ul> -->

    <Connect />
  </div>
</div>
