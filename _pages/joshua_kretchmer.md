<!-- People page styling (this file renders first on /people/, so the styles apply to the whole page). -->

{% include_relative page_title_style.html %}

<style>
  /* Spacing between people */
  article hr { margin: 2.75rem 0 2rem; }
  /* Names and section headings (normal text color) */
  article .clearfix h2 { font-weight: 700; font-size: 2.25rem; color: var(--global-text-color); margin: 0 0 0.75rem; }
  /* Bios */
  article .clearfix p { font-size: 1.125rem; line-height: 1.7; }
  /* Role + contact under each photo */
  .profile { margin-bottom: 1.25rem; }
  .profile .more-info { font-family: inherit; margin-top: 0.75rem; }
  .profile .more-info p { display: block; margin: 0 0 0.35rem; font-size: 1.05rem; line-height: 1.5; }
  .profile .more-info .role { font-size: 0.95rem; font-weight: 700; letter-spacing: 0.08em; text-transform: uppercase; color: var(--global-text-color); margin-bottom: 0.6rem; }
  .profile .more-info .contact i { width: 1.4em; color: var(--global-theme-color); }
  /* Former members: cards */
  .former-members { list-style: none; padding: 0; margin: 1.25rem 0 0; display: grid; grid-template-columns: repeat(auto-fit, minmax(19rem, 1fr)); gap: 1rem; }
  .former-members li { padding: 1rem 1.25rem; border-left: 0.3rem solid var(--global-theme-color); border-radius: 0.25rem; background: var(--global-card-bg-color); line-height: 1.5; }
  .former-members span { display: block; }
  .former-members .fm-name { font-size: 1.25rem; font-weight: 700; color: var(--global-text-color); }
  .former-members .fm-role { font-size: 0.95rem; font-weight: 600; text-transform: uppercase; letter-spacing: 0.05em; color: var(--global-text-color); margin: 0.15rem 0 0.4rem; }
  .former-members .fm-now { font-size: 1.05rem; }
</style>

<a id="josh"></a>

## Joshua Kretchmer

Joshua Kretchmer was born in San Jose, Costa Rica and grew up in Mill Valley, CA. He received his B.S. in Chemistry from UC Berkeley in 2009 and his Ph.D. as an NSF graduate research fellow from Caltech in December 2014 under the mentorship of Prof. Thomas Miller. He left Caltech for Princeton to join the group of Garnet Chan as a postdoctoral scholar. After the Chan group relocated to Caltech, he returned to finish his postdoctoral work there. He joined the faculty of the Georgia Institute of Technology in 2019.
