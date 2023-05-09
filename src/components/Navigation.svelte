<nav>
  <ul>
    <li><button id="cv" aria-label="See my CV" tabindex="0">CV</button></li>
    <li>
      <button id="blog" aria-label="Read my blog" tabindex="0">Blog</button>
    </li>
    <li>
      <button id="about" aria-label="Read about me" tabindex="0"
        >About me</button
      >
    </li>
  </ul>
</nav>

<style lang="scss">
  @import "../styles/_variables.scss";

  nav {
    grid-row: 2;
    grid-column: 1 / span 2;
    background: transparent;
    border-right: 1px solid var(--secondary);
    border-top: 1px solid var(--secondary);

    @media screen and (max-width: $mobile-breakpoint) {
      grid-row: 4;
      grid-column: 1;
    }

    ul {
      margin: 0;
      padding: 0;
      list-style-type: none;

      li {
        position: relative;

        border-bottom: 1px solid var(--secondary);

        background-image: linear-gradient(var(--secondary), var(--secondary));
        background-size: 0 100%;
        background-repeat: no-repeat;

        transition: all 0.4s ease-in-out;

        @media (prefers-color-scheme: dark) {
          background-image: linear-gradient(var(--black), var(--black));
        }

        &:hover {
          background-size: 100% 100%;
          color: var(--primary);
          @media (prefers-reduced-motion: reduce) {
            background-size: 0 100%;
          }
        }

        button {
          color: var(--secondary);

          padding: 1rem 4rem;

          border: none;

          background: transparent;

          font-size: 2.5rem;
          text-align: left;

          width: 100%;

          cursor: pointer;

          &:hover {
            color: var(--white);
          }
        }
      }
    }
  }
</style>
