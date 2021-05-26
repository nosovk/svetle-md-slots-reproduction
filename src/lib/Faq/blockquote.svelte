<script lang="ts">
  let open: boolean;
  export let question;
</script>

<div class="dropdown">
  <div class="row">
    <div class="col action" on:click={() => (open = !open)}>
      <span class:open />
    </div>
    <div class="col">
      <p class="title"><slot name="question">{question}</slot></p>
    </div>
  </div>
  <div class="issue" class:open>
    <slot />
  </div>
</div>

<style lang="scss">
  .dropdown {
    margin-bottom: 0.5rem;
    border-radius: var(--br-16);
    background-color: var(--color-white);

    .row {
      padding: 1rem 2.5rem 1rem 1rem;
      position: relative;
      z-index: 1;

      .col {
        @extend %flex-center;

        &.action {
          padding: 1rem;
          min-height: 2rem;
          cursor: pointer;

          span {
            position: relative;
            display: block;
            width: 1.688rem;
            height: 1.688rem;
            margin: 0 1.5rem;

            &::before {
              position: absolute;
              height: 1.688rem;
              width: 0.125rem;
              left: 0;
              top: 0;
              background-color: var(--color-icon-more);
              content: '';
            }

            &::after {
              position: absolute;
              height: 1.688rem;
              width: 0.125rem;
              left: 0;
              top: 0;
              transform: rotate(90deg);
              background-color: var(--color-icon-more);
              content: '';
            }

            &.open {
              &::before {
                display: none;
              }
            }
          }
        }

        .title {
          @include font(var(--size-14), var(--weight-700), var(--color-text-dark));
        }
      }
    }

    .issue {
      position: relative;
      height: 0;
      top: -8rem;
      opacity: 0;
      padding: 0;
      @include font(var(--size-12), var(--weight-400), var(--color-text-white));
      background-color: var(--color-dark);
      transition: top 0.3s, opacity 0.3s, padding 0.3s, height 0.3s;

      &.open {
        position: relative;
        top: 0;
        opacity: 1;
        padding: 1rem 2.5rem;
        height: max-content;
        transition: top 0.3s, opacity 0.3s, padding 0.3s, height 0.3s;
      }


    }
  }


  :global(a) { // readme: https://github.com/pngwn/MDsveX/issues/107
    @include font(var(--size-12), var(--weight-400), var(--color-text-white));

    &:hover {
      text-decoration: none;
    }
  }

  @media (min-width: $min-width-medium) {
    .dropdown {
      .row {
        z-index: unset;
      }
    }
  }
</style>
