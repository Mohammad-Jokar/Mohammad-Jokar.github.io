---
layout: default
title: Publications
permalink: /publications/
---

{% include navigation.html %}

<style>
/* =========================================================
   PUBLICATIONS PAGE
   ========================================================= */

.publications-page {
  --pub-primary: #123c69;
  --pub-secondary: #007f86;
  --pub-accent: #e58b33;
  --pub-soft-blue: #eef6fa;
  --pub-soft-green: #edf8f5;
  --pub-soft-orange: #fff5e9;
  --pub-text: #233142;
  --pub-muted: #66788a;
  --pub-border: #dce6ec;
  --pub-white: #ffffff;

  width: 100%;
  color: var(--pub-text);
  line-height: 1.7;
}

.publications-page * {
  box-sizing: border-box;
}

/* =========================================================
   HERO SECTION
   ========================================================= */

.publications-hero {
  position: relative;
  overflow: hidden;
  margin: 1.5rem 0 2.5rem;
  padding: 3.6rem 2.5rem;
  color: white;
  background:
    radial-gradient(
      circle at 90% 20%,
      rgba(255, 255, 255, 0.18),
      transparent 25%
    ),
    linear-gradient(
      135deg,
      #103b66 0%,
      #006f78 58%,
      #0f8f83 100%
    );
  border-radius: 28px;
  box-shadow: 0 20px 50px rgba(18, 60, 105, 0.18);
}

.publications-hero::before {
  content: "";
  position: absolute;
  top: -80px;
  right: 80px;
  width: 190px;
  height: 190px;
  background: rgba(255, 255, 255, 0.06);
  border-radius: 50%;
}

.publications-hero::after {
  content: "";
  position: absolute;
  right: -90px;
  bottom: -120px;
  width: 310px;
  height: 310px;
  border: 45px solid rgba(255, 255, 255, 0.08);
  border-radius: 50%;
}

.publications-hero-content {
  position: relative;
  z-index: 2;
  max-width: 800px;
}

.publications-kicker {
  display: inline-block;
  margin-bottom: 0.8rem;
  padding: 0.35rem 0.85rem;
  color: white;
  background: rgba(255, 255, 255, 0.15);
  border: 1px solid rgba(255, 255, 255, 0.28);
  border-radius: 999px;
  font-size: 0.82rem;
  font-weight: 700;
  letter-spacing: 0.08em;
  text-transform: uppercase;
}

.publications-hero h1 {
  margin: 0 0 1rem;
  color: white;
  font-size: clamp(2.35rem, 6vw, 4rem);
  line-height: 1.08;
  letter-spacing: -0.04em;
}

.publications-hero p {
  max-width: 720px;
  margin: 0;
  color: rgba(255, 255, 255, 0.92);
  font-size: 1.08rem;
}

.hero-actions {
  display: flex;
  flex-wrap: wrap;
  gap: 0.8rem;
  margin-top: 1.6rem;
}

.hero-button {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  gap: 0.45rem;
  padding: 0.72rem 1.1rem;
  color: var(--pub-primary) !important;
  background: white;
  border: 1px solid white;
  border-radius: 12px;
  font-size: 0.92rem;
  font-weight: 700;
  text-decoration: none !important;
  transition:
    transform 0.2s ease,
    box-shadow 0.2s ease,
    background 0.2s ease;
}

.hero-button:hover {
  transform: translateY(-2px);
  box-shadow: 0 10px 25px rgba(0, 0, 0, 0.15);
}

.hero-button.secondary {
  color: white !important;
  background: transparent;
  border-color: rgba(255, 255, 255, 0.55);
}

.hero-button.secondary:hover {
  color: var(--pub-primary) !important;
  background: white;
}

/* =========================================================
   RESEARCH FOCUS CARDS
   ========================================================= */

.research-focus-grid {
  display: grid;
  grid-template-columns: repeat(4, minmax(0, 1fr));
  gap: 1rem;
  margin: 0 0 3rem;
}

.focus-card {
  padding: 1.3rem;
  background: white;
  border: 1px solid var(--pub-border);
  border-radius: 18px;
  box-shadow: 0 8px 25px rgba(25, 55, 75, 0.06);
  transition:
    transform 0.2s ease,
    box-shadow 0.2s ease,
    border-color 0.2s ease;
}

.focus-card:hover {
  transform: translateY(-4px);
  border-color: #a8cbd6;
  box-shadow: 0 14px 30px rgba(25, 55, 75, 0.11);
}

.focus-icon {
  margin-bottom: 0.55rem;
  font-size: 1.65rem;
}

.focus-card h3 {
  margin: 0 0 0.35rem;
  color: var(--pub-primary);
  font-size: 1rem;
}

.focus-card p {
  margin: 0;
  color: var(--pub-muted);
  font-size: 0.86rem;
  line-height: 1.5;
}

/* =========================================================
   GENERAL SECTIONS
   ========================================================= */

.publication-section {
  scroll-margin-top: 100px;
  margin: 3.25rem 0;
}

.section-heading {
  display: flex;
  align-items: flex-end;
  justify-content: space-between;
  gap: 1rem;
  margin-bottom: 1.35rem;
  padding-bottom: 0.75rem;
  border-bottom: 1px solid var(--pub-border);
}

.section-heading h2 {
  margin: 0;
  color: var(--pub-primary);
  font-size: 1.65rem;
  line-height: 1.25;
}

.section-heading p {
  max-width: 420px;
  margin: 0;
  color: var(--pub-muted);
  font-size: 0.88rem;
  text-align: right;
}

/* =========================================================
   FEATURED PUBLICATION
   ========================================================= */

.featured-publication {
  display: grid;
  grid-template-columns: 105px minmax(0, 1fr);
  gap: 1.5rem;
  padding: 1.8rem;
  background: linear-gradient(135deg, var(--pub-soft-blue), white);
  border: 1px solid #cfe1eb;
  border-radius: 22px;
  box-shadow: 0 12px 35px rgba(18, 60, 105, 0.08);
}

.featured-year {
  display: flex;
  align-items: center;
  justify-content: center;
  min-height: 105px;
  color: white;
  background: linear-gradient(
    145deg,
    var(--pub-primary),
    var(--pub-secondary)
  );
  border-radius: 18px;
  font-size: 1.35rem;
  font-weight: 800;
}

.featured-publication h3 {
  margin: 0.45rem 0 0.65rem;
  color: var(--pub-primary);
  font-size: 1.3rem;
  line-height: 1.35;
}

.featured-publication p {
  margin: 0.3rem 0;
}

/* =========================================================
   PUBLICATION CARDS
   ========================================================= */

.publication-grid {
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  gap: 1.1rem;
}

.publication-card {
  position: relative;
  display: flex;
  flex-direction: column;
  min-height: 100%;
  padding: 1.45rem;
  background: white;
  border: 1px solid var(--pub-border);
  border-radius: 18px;
  box-shadow: 0 7px 20px rgba(40, 60, 75, 0.055);
  transition:
    transform 0.22s ease,
    box-shadow 0.22s ease,
    border-color 0.22s ease;
}

.publication-card:hover {
  transform: translateY(-4px);
  border-color: #9fc6d4;
  box-shadow: 0 15px 35px rgba(24, 75, 96, 0.12);
}

.publication-meta {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 0.7rem;
  margin-bottom: 0.8rem;
}

.publication-year {
  color: var(--pub-primary);
  font-weight: 800;
}

.publication-type {
  padding: 0.25rem 0.62rem;
  color: #086a68;
  background: var(--pub-soft-green);
  border-radius: 999px;
  font-size: 0.72rem;
  font-weight: 700;
  text-align: center;
}

.publication-card h3 {
  margin: 0 0 0.8rem;
  color: var(--pub-primary);
  font-size: 1.06rem;
  line-height: 1.42;
}

.publication-authors {
  margin: 0.25rem 0;
  color: #465b6b;
  font-size: 0.88rem;
}

.publication-journal {
  margin: 0.25rem 0 0;
  color: var(--pub-muted);
  font-size: 0.88rem;
}

.publication-tags {
  display: flex;
  flex-wrap: wrap;
  gap: 0.38rem;
  margin-top: 1rem;
}

.publication-tag {
  padding: 0.22rem 0.55rem;
  color: #526878;
  background: #f1f5f7;
  border-radius: 6px;
  font-size: 0.7rem;
  font-weight: 600;
}

.publication-link {
  display: inline-flex;
  align-items: center;
  width: fit-content;
  margin-top: auto;
  padding-top: 1rem;
  color: var(--pub-secondary) !important;
  font-size: 0.84rem;
  font-weight: 750;
  text-decoration: none !important;
}

.publication-link:hover {
  color: var(--pub-primary) !important;
  text-decoration: underline !important;
}

/* =========================================================
   GLOBAL BURDEN OF DISEASE SECTION
   ========================================================= */

.gbd-panel {
  padding: 2rem;
  color: white;
  background: linear-gradient(
    135deg,
    rgba(18, 60, 105, 0.97),
    rgba(0, 127, 134, 0.94)
  );
  border-radius: 24px;
  box-shadow: 0 15px 40px rgba(18, 60, 105, 0.14);
}

.gbd-panel h2,
.gbd-panel h3 {
  color: white;
}

.gbd-panel > p {
  max-width: 850px;
  color: rgba(255, 255, 255, 0.89);
}

.gbd-list {
  display: grid;
  gap: 0.75rem;
  margin-top: 1.4rem;
}

.gbd-item {
  padding: 1rem 1.1rem;
  background: rgba(255, 255, 255, 0.1);
  border: 1px solid rgba(255, 255, 255, 0.16);
  border-radius: 13px;
  transition:
    transform 0.2s ease,
    background 0.2s ease;
}

.gbd-item:hover {
  transform: translateX(4px);
  background: rgba(255, 255, 255, 0.15);
}

.gbd-item strong {
  display: block;
  margin-bottom: 0.25rem;
  color: white;
}

.gbd-item span {
  color: rgba(255, 255, 255, 0.78);
  font-size: 0.84rem;
}

/* =========================================================
   ACADEMIC PROFILE LINKS
   ========================================================= */

.profile-panel {
  margin: 3.5rem 0 1rem;
  padding: 2rem;
  text-align: center;
  background: var(--pub-soft-orange);
  border: 1px solid #f0dcc4;
  border-radius: 24px;
}

.profile-panel h2 {
  margin-top: 0;
  color: var(--pub-primary);
}

.profile-panel p {
  max-width: 680px;
  margin: 0 auto 1.4rem;
  color: var(--pub-muted);
}

.profile-links {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 0.75rem;
}

.profile-link {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  padding: 0.68rem 1rem;
  color: white !important;
  background: var(--pub-primary);
  border-radius: 10px;
  font-size: 0.88rem;
  font-weight: 700;
  text-decoration: none !important;
  transition:
    transform 0.2s ease,
    background 0.2s ease,
    box-shadow 0.2s ease;
}

.profile-link:hover {
  transform: translateY(-2px);
  background: var(--pub-secondary);
  box-shadow: 0 8px 20px rgba(18, 60, 105, 0.16);
}

.publications-note {
  margin-top: 1.5rem;
  color: var(--pub-muted);
  font-size: 0.78rem;
  text-align: center;
}

/* =========================================================
   RESPONSIVE DESIGN
   ========================================================= */

@media (max-width: 900px) {
  .research-focus-grid {
    grid-template-columns: repeat(2, minmax(0, 1fr));
  }

  .publication-grid {
    grid-template-columns: 1fr;
  }
}

@media (max-width: 650px) {
  .publications-hero {
    padding: 2.4rem 1.4rem;
    border-radius: 20px;
  }

  .publications-hero h1 {
    font-size: 2.5rem;
  }

  .research-focus-grid {
    grid-template-columns: 1fr;
  }

  .featured-publication {
    grid-template-columns: 1fr;
  }

  .featured-year {
    min-height: 65px;
  }

  .section-heading {
    display: block;
  }

  .section-heading p {
    margin-top: 0.45rem;
    text-align: left;
  }

  .publication-meta {
    align-items: flex-start;
  }

  .hero-actions,
  .profile-links {
    flex-direction: column;
    align-items: stretch;
  }

  .hero-button,
  .profile-link {
    width: 100%;
  }

  .gbd-panel,
  .profile-panel {
    padding: 1.4rem;
    border-radius: 18px;
  }
}
</style>

<div class="publications-page">

  <!-- =====================================================
       HERO
       ===================================================== -->

  <section class="publications-hero">
    <div class="publications-hero-content">

      <span class="publications-kicker">
        Research · Collaboration · Impact
      </span>

      <h1>Publications</h1>

      <p>
        My research connects veterinary medicine, antimicrobial resistance,
        epidemiology, infodemiology, health communication, One Health, and
        global burden of disease research.
      </p>

      <div class="hero-actions">

        <a
          class="hero-button"
          href="https://orcid.org/0000-0003-4888-4119"
          target="_blank"
          rel="noopener noreferrer"
        >
          View ORCID ↗
        </a>

        #selected-publications
          Explore selected publications ↓
        </a>

      </div>
    </div>
  </section>

  <!-- =====================================================
       RESEARCH AREAS
       ===================================================== -->

  <section class="research-focus-grid">

    <article class="focus-card">
      <div class="focus-icon" aria-hidden="true">🦠</div>

      <h3>Antimicrobial Resistance</h3>

      <p>
        AMR surveillance, antimicrobial use, resistance-related practices,
        and evidence synthesis.
      </p>
    </article>

    <article class="focus-card">
      <div class="focus-icon" aria-hidden="true">🐾</div>

      <h3>Veterinary Medicine</h3>

      <p>
        Companion-animal health, infectious disease, emergency care,
        reproduction, and epidemiology.
      </p>
    </article>

    <article class="focus-card">
      <div class="focus-icon" aria-hidden="true">📈</div>

      <h3>Infodemiology</h3>

      <p>
        Google Trends, social-media analysis, public search behaviour,
        and risk communication.
      </p>
    </article>

    <article class="focus-card">
      <div class="focus-icon" aria-hidden="true">🌍</div>

      <h3>Global Health</h3>

      <p>
        One Health, population health, systematic reviews, and Global
        Burden of Disease collaborations.
      </p>
    </article>

  </section>

  <!-- =====================================================
       FEATURED PUBLICATION
       ===================================================== -->

  <section class="publication-section">

    <div class="section-heading">

      <h2>Featured Research</h2>

      <p>
        Research connecting veterinary epidemiology,
        antimicrobial stewardship, and One Health.
      </p>

    </div>

    <article class="featured-publication">

      <div class="featured-year">
        2026
      </div>

      <div>

        <span class="publication-type">
          First author
        </span>

        <h3>
          Impact of the Colistin Ban on Antimicrobial Use and
          Resistance-Related Practices Among Layer Farmers in Indonesia:
          A Comparative KAP Study
        </h3>

        <p class="publication-authors">
          <strong>Mohammad Jokar</strong>, Sunandar, Annisa Rachmawati,
          Soe Yu Naing, Happy Nanda Larasati, Ridvana Dwibawa Darmawan,
          and colleagues.
        </p>

        <p class="publication-journal">
          <em>Frontiers in Veterinary Science</em>.
          2026;13:1885994.
        </p>

        <div class="publication-tags">

          <span class="publication-tag">
            Antimicrobial resistance
          </span>

          <span class="publication-tag">
            Veterinary public health
          </span>

          <span class="publication-tag">
            KAP study
          </span>

          <span class="publication-tag">
            One Health
          </span>

        </div>

      </div>
    </article>

  </section>

  <!-- =====================================================
       FIRST-AUTHORED PUBLICATIONS
       ===================================================== -->

  <section
    class="publication-section"
    id="selected-publications"
  >

    <div class="section-heading">

      <h2>Selected First-Authored Publications</h2>

      <p>
        Selected studies highlighting the breadth and development
        of my research.
      </p>

    </div>

    <div class="publication-grid">

      <!-- Publication 1 -->

      <article class="publication-card">

        <div class="publication-meta">

          <span class="publication-year">
            2026
          </span>

          <span class="publication-type">
            Veterinary epidemiology
          </span>

        </div>

        <h3>
          Identified-but-Unaccompanied Dogs and Cats During the
          2026 Iran War in Tehran
        </h3>

        <p class="publication-authors">
          <strong>Mohammad Jokar</strong>, Mobina Payami,
          Arman Abdous, and Diego B. Nobrega.
        </p>

        <p class="publication-journal">
          <em>
            Preventive Veterinary Medicine:
            Regional Studies and Reports
          </em>.
          2026;100054.
        </p>

        <div class="publication-tags">

          <span class="publication-tag">
            Animal welfare
          </span>

          <span class="publication-tag">
            Emergency response
          </span>

          <span class="publication-tag">
            Companion animals
          </span>

        </div>

      </article>

      <!-- Publication 2 -->

      <article class="publication-card">

        <div class="publication-meta">

          <span class="publication-year">
            2026
          </span>

          <span class="publication-type">
            Infodemiology
          </span>

        </div>

        <h3>
          Infodemiology of Public Sentiment Toward the Measles Vaccine
          in Canada: A Google Trends and Health Belief Model-Based Analysis
        </h3>

        <p class="publication-authors">
          <strong>Mohammad Jokar</strong>, Quinn Goddard,
          and Diego Nobrega.
        </p>

        <p class="publication-journal">
          <em>Vaccine</em>.
          2026;69:127998.
        </p>

        <div class="publication-tags">

          <span class="publication-tag">
            Measles vaccine
          </span>

          <span class="publication-tag">
            Google Trends
          </span>

          <span class="publication-tag">
            Canada
          </span>

        </div>

      </article>

      <!-- Publication 3 -->

      <article class="publication-card">

        <div class="publication-meta">

          <span class="publication-year">
            2025
          </span>

          <span class="publication-type">
            Health communication
          </span>

        </div>

        <h3>
          Analyzing Public Google Search Interest in Measles Within Canada:
          Identifying Key Moments for Targeted Risk Communication
        </h3>

        <p class="publication-authors">
          <strong>Mohammad Jokar</strong> and Diego Nobrega.
        </p>

        <p class="publication-journal">
          <em>Journal of Medical Internet Research</em>.
          2025;27:e75025.
        </p>

        <div class="publication-tags">

          <span class="publication-tag">
            Risk communication
          </span>

          <span class="publication-tag">
            Infodemiology
          </span>

          <span class="publication-tag">
            Public health
          </span>

        </div>

        https://www.jmir.org/2025/1/e75025
          View publication ↗
        </a>

      </article>

      <!-- Publication 4 -->

      <article class="publication-card">

        <div class="publication-meta">

          <span class="publication-year">
            2024
          </span>

          <span class="publication-type">
            Veterinary AI
          </span>

        </div>

        <h3>
          AI Chatbots in Pet Health Care:
          Opportunities and Challenges for Owners
        </h3>

        <p class="publication-authors">
          <strong>Mohammad Jokar</strong>, Arman Abdous,
          and Vahid Rahmanian.
        </p>

        <p class="publication-journal">
          <em>Veterinary Medicine and Science</em>.
          2024;10(3).
        </p>

        <div class="publication-tags">

          <span class="publication-tag">
            Artificial intelligence
          </span>

          <span class="publication-tag">
            Pet health
          </span>

          <span class="publication-tag">
            Chatbots
          </span>

        </div>

      </article>

      <!-- Publication 5 -->

      <article class="publication-card">

        <div class="publication-meta">

          <span class="publication-year">
            2023
          </span>

          <span class="publication-type">
            Systematic review
          </span>

        </div>

        <h3>
          The Global Seroprevalence of Equine Brucellosis:
          A Systematic Review and Meta-analysis Based on
          Publications From 1990 to 2022
        </h3>

        <p class="publication-authors">
          <strong>Mohammad Jokar</strong>, Vahid Rahmanian,
          Nadia Golestani, Yasamin Raziee, and Mehran Farhoodi.
        </p>

        <p class="publication-journal">
          <em>Journal of Equine Veterinary Science</em>.
          2023;123:104227.
        </p>

        <div class="publication-tags">

          <span class="publication-tag">
            Brucellosis
          </span>

          <span class="publication-tag">
            Equine health
          </span>

          <span class="publication-tag">
            Meta-analysis
          </span>

        </div>

      </article>

      <!-- Publication 6 -->

      <article class="publication-card">

        <div class="publication-meta">

          <span class="publication-year">
            2021
          </span>

          <span class="publication-type">
            Veterinary parasitology
          </span>

        </div>

        <h3>
          Neospora caninum Infection in Cattle and Dogs in Iran:
          A Systematic Review and Meta-analysis
        </h3>

        <p class="publication-authors">
          <strong>Mohammad Jokar</strong>, Saied Bokaie,
          Vahid Rahmanian, Razieh Zahedi, and colleagues.
        </p>

        <p class="publication-journal">
          <em>
            American Journal of Animal and Veterinary Sciences
          </em>.
          2021;16(1):23–38.
        </p>

        <div class="publication-tags">

          <span class="publication-tag">
            Neospora caninum
          </span>

          <span class="publication-tag">
            Cattle
          </span>

          <span class="publication-tag">
            Dogs
          </span>

        </div>

      </article>

    </div>
  </section>

  <!-- =====================================================
       COLLABORATIVE PUBLICATIONS
       ===================================================== -->

  <section class="publication-section">

    <div class="section-heading">

      <h2>Selected Collaborative Publications</h2>

      <p>
        Interdisciplinary research across veterinary medicine,
        infectious disease, AMR, and public health.
      </p>

    </div>

    <div class="publication-grid">

      <!-- Collaborative publication 1 -->

      <article class="publication-card">

        <div class="publication-meta">

          <span class="publication-year">
            2026
          </span>

          <span class="publication-type">
            One Health education
          </span>

        </div>

        <h3>
          Faculty Perspectives on One Health: Insights From a
          Transdisciplinary Networking Event at the University of Calgary
        </h3>

        <p class="publication-authors">
          <strong>Mohammad Jokar</strong>, Samantha Larose-Berry,
          and Karin Orsel.
        </p>

        <p class="publication-journal">
          <em>The Canadian Veterinary Journal</em>.
          2026;67(2):228.
        </p>

        <div class="publication-tags">

          <span class="publication-tag">
            One Health
          </span>

          <span class="publication-tag">
            Education
          </span>

          <span class="publication-tag">
            Collaboration
          </span>

        </div>

      </article>

      <!-- Collaborative publication 2 -->

      <article class="publication-card">

        <div class="publication-meta">

          <span class="publication-year">
            2025
          </span>

          <span class="publication-type">
            Rabies epidemiology
          </span>

        </div>

        <h3>
          Incidence and Prevalence of Rabies Virus Infections in
          Tested Humans and Animals in Asia: A Systematic Review
          and Meta-analysis
        </h3>

        <p class="publication-authors">
          Farzane Shams, <strong>Mohammad Jokar</strong>,
          Ehssan Djalali, Arman Abdous, and colleagues.
        </p>

        <p class="publication-journal">
          <em>One Health</em>.
          2025;20:101102.
        </p>

        <div class="publication-tags">

          <span class="publication-tag">
            Rabies
          </span>

          <span class="publication-tag">
            Asia
          </span>

          <span class="publication-tag">
            One Health
          </span>

        </div>

      </article>

      <!-- Collaborative publication 3 -->

      <article class="publication-card">

        <div class="publication-meta">

          <span class="publication-year">
            2025
          </span>

          <span class="publication-type">
            Antimicrobial resistance
          </span>

        </div>

        <h3>
          Global Knowledge, Attitudes, and Practices Towards
          Antimicrobial Resistance Among Healthcare Workers:
          A Systematic Review and Meta-analysis
        </h3>

        <p class="publication-authors">
          Abdolreza Sotoodeh Jahromi, Negin Namavari,
          <strong>Mohammad Jokar</strong>, and colleagues.
        </p>

        <p class="publication-journal">
          <em>Antimicrobial Resistance &amp; Infection Control</em>.
          2025;14:47.
        </p>

        <div class="publication-tags">

          <span class="publication-tag">
            AMR
          </span>

          <span class="publication-tag">
            Healthcare workers
          </span>

          <span class="publication-tag">
            Evidence synthesis
          </span>

        </div>

      </article>

      <!-- Collaborative publication 4 -->

      <article class="publication-card">

        <div class="publication-meta">

          <span class="publication-year">
            2024
          </span>

          <span class="publication-type">
            Veterinary infectious disease
          </span>

        </div>

        <h3>
          Seroprevalence of Toxoplasma gondii and Neospora spp.
          in the Horse Population of Tehran, Iran
        </h3>

        <p class="publication-authors">
          Farzane Shams, <strong>Mohammad Jokar</strong>,
          Arman Abdous, Pardis Mohammadi, and colleagues.
        </p>

        <p class="publication-journal">
          <em>Scientific Reports</em>.
          2024;14:17054.
        </p>

        <div class="publication-tags">

          <span class="publication-tag">
            Toxoplasma
          </span>

          <span class="publication-tag">
            Neospora
          </span>

          <span class="publication-tag">
            Equine health
          </span>

        </div>

      </article>

    </div>
  </section>

  <!-- =====================================================
       GLOBAL BURDEN OF DISEASE
       ===================================================== -->

  <section class="publication-section gbd-panel">

    <h2>Global Burden of Disease Collaborations</h2>

    <p>
      I contribute to large-scale collaborative research examining
      disease burden, antimicrobial resistance, population health,
      mortality, risk factors, and health-system priorities across
      countries and regions.
    </p>

    <div class="gbd-list">

      <div class="gbd-item">

        <strong>
          Global Burden of Bacterial Antimicrobial Resistance,
          1990–2021
        </strong>

        <span>
          <em>The Lancet</em>, 2024
        </span>

      </div>

      <div class="gbd-item">

        <strong>
          Burden of 375 Diseases and Injuries and 88 Risk Factors,
          1990–2023
        </strong>

        <span>
          <em>The Lancet</em>, 2025
        </span>

      </div>

      <div class="gbd-item">

        <strong>
          Global Burden of Meningitis, Its Risk Factors,
          and Aetiologies, 1990–2023
        </strong>

        <span>
          <em>The Lancet Neurology</em>, 2026
        </span>

      </div>

      <div class="gbd-item">

        <strong>
          Global Burden of Cardiovascular Diseases and
          Risk Factors, 1990–2023
        </strong>

        <span>
          <em>
            Journal of the American College of Cardiology
          </em>,
          2025
        </span>

      </div>

    </div>
  </section>

  <!-- =====================================================
       COMPLETE PUBLICATION RECORD
       ===================================================== -->

  <section class="profile-panel">

    <h2>Complete Publication Record</h2>

    <p>
      For the complete and most current list of publications,
      citation information, collaborators, and research outputs,
      visit my academic profiles.
    </p>

    <div class="profile-links">

      <a
        class="profile-link"
        href="https://orcid.org/0000-0003-4888-4119"
        target="_blank"
        rel="noopener noreferrer"
      >
        ORCID ↗
      </a>

      <a
        class="profile-link"
        href="https://www.researchgate.net/profile/Mohammad-Jokar-6"
        target="_blank"
        rel="noopener noreferrer"
      >
        ResearchGate ↗
      </a>

      <!-- Replace this address with your personal Google Scholar URL. -->
      https://scholar.google.com/
        Google Scholar ↗
      </a>

    </div>

    <div class="publications-note">
      Publication details are updated periodically. Please consult
      the publisher's website for final citation information.
    </div>

  </section>

</div>
