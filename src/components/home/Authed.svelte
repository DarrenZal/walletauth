<script lang="ts">
  import { sessionStore } from '$src/stores'

  const start_and_end = (str: string) => {
    if (str.length > 35) {
      return str.substr(0, 5) + '.....' + str.substr(str.length-4, str.length)
    }
    return str
  }
</script>

<div
  class="min-h-[calc(100vh-128px)] md:min-h-[calc(100vh-160px)] pt-8 md:pt-16 flex flex-col items-start max-w-[690px] m-auto gap-10 pb-5 text-sm"
>
  <h1 class="text-xl">Welcome, <span class="font-bold uppercase">{start_and_end($sessionStore.address)}</span>!</h1>

  <div class="flex flex-col items-start justify-center gap-5">
    <h2 class="text-lg">ReFi Chat</h2>
    <p>
      ReFi Chat is a chatbot that answers questions about Regenerative Finance (ReFi).<br>
      It combines a knowledge graph with a Large Language Model to provide verifiable answers.
      Previous prompts and replies are not kept in context for new prompts, to save costs.<br>
      Feel free to <a class="blue-link" href="/Chat">Submit Feedback</a> directly in the app, or reach out to <a class="blue-link" href="https://twitter.com/zaldarren" target="_blank" rel="noreferrer">Darren Zal</a>.<br>
      Check out the code on <a class="blue-link" href="https://github.com/DarrenZal/NatLangKG" target="_blank" rel="noreferrer">GitHub</a>
    </p>
    <a class="btn btn-primary" href="/Chat">Try ReFi Chat</a>
  </div>
</div>
<style>
  .blue-link {
    color: blue;
    text-decoration: underline;
    cursor: pointer;
  }
</style>