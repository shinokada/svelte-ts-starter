<script>
  import { Alert } from "flowbite-svelte";
  import { format } from "timeago.js";
  import Card from "./Card.svelte";
  import { blogs } from "../data";
</script>

<h1 class="text-3xl dark:text-white">Lorem ipsum dolor sit amet</h1>
{#each blogs as blog, i}
  <Card
    title={blog.title}
    description={blog.content}
    image={blog.image}
    publishDate={format(blog.publishDate)}
  />
{/each}

<Alert dismissable>
  <span slot="icon"
    ><svg
      aria-hidden="true"
      class="w-5 h-5"
      fill="currentColor"
      viewBox="0 0 20 20"
      xmlns="http://www.w3.org/2000/svg"
      ><path
        fill-rule="evenodd"
        d="M18 10a8 8 0 11-16 0 8 8 0 0116 0zm-7-4a1 1 0 11-2 0 1 1 0 012 0zM9 9a1 1 0 000 2v3a1 1 0 001 1h1a1 1 0 100-2v-3a1 1 0 00-1-1H9z"
        clip-rule="evenodd"
      /></svg
    >
  </span>
  A simple info alert with an
  <a
    href="/"
    class="font-semibold underline hover:text-blue-800 dark:hover:text-blue-900"
    >example link</a
  >. Give it a click if you like.
</Alert>
