<script>
  let isFollowing = false;
</script>

<button
  class={isFollowing ? "is-active" : ""}
  on:click={() => (isFollowing = !isFollowing)}
>
  {isFollowing ? "Unfollow" : "Follow"}
</button>

<style lang="scss">
  button {
    --follow-color: cornflowerblue;
    --unfollow-color: firebrick;

    background-color: #fff;
    border-radius: 9999px;
    border: 1px solid var(--follow-color);
    color: var(--follow-color);
    cursor: pointer;
    font-size: x-small;
    padding: 4px 16px;
    text-transform: uppercase;
    transition: background-color 125ms ease-out;

    &:hover {
      background-color: var(--follow-color);
      color: #fff;
      transition-timing-function: ease-in;
    }

    &.is-active {
      border-color: var(--unfollow-color);
      color: var(--unfollow-color);

      &:hover {
        background-color: var(--unfollow-color);
        color: #fff;
      }
    }
  }
</style>
