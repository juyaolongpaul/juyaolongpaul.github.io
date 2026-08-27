---
layout: page
title: MMR Lab
permalink: /mmr-lab/
description: Multimodal Music Research Lab
nav: true
nav_order: 7
_styles: |
  .mmr-lab {
    --mmr-blue: #073f9e;
    --mmr-blue-soft: rgba(7, 63, 158, 0.08);
    --mmr-line: var(--global-divider-color);
  }

  .post-header {
    display: none;
  }

  .mmr-hero {
    margin: 0 0 2rem;
    padding: 1.5rem 0 1.75rem;
    border-bottom: 1px solid var(--mmr-line);
  }

  .mmr-hero h1 {
    margin: 0 0 0.55rem;
    font-size: 2rem;
    font-weight: 700;
    letter-spacing: 0;
  }

  .mmr-hero .lead {
    max-width: 48rem;
    margin-bottom: 0;
    color: var(--global-text-color);
    font-size: 1.05rem;
    line-height: 1.65;
  }

  .mmr-section {
    margin: 2.2rem 0;
  }

  .mmr-section h2 {
    margin: 0 0 1rem;
    color: var(--global-text-color);
    font-size: 1.45rem;
    font-weight: 700;
    letter-spacing: 0;
  }

  .mmr-news {
    margin: 0;
    padding: 0;
    list-style: none;
    border-top: 1px solid var(--mmr-line);
  }

  .mmr-news li {
    display: grid;
    grid-template-columns: 7rem 1fr;
    gap: 1rem;
    padding: 0.7rem 0;
    border-bottom: 1px solid var(--mmr-line);
    line-height: 1.45;
  }

  .mmr-news time {
    color: var(--global-text-color-light);
    font-weight: 700;
  }

  .mmr-team-group {
    margin-top: 1.8rem;
  }

  .mmr-team-group h3 {
    margin: 0 0 1rem;
    color: var(--global-text-color);
    font-size: 1.12rem;
    font-weight: 700;
  }

  .mmr-team-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(13.5rem, 1fr));
    gap: 1rem;
  }

  .mmr-member {
    display: flex;
    gap: 0.9rem;
    min-height: 9.2rem;
    padding: 1rem;
    border: 1px solid var(--mmr-line);
    border-radius: 8px;
    background: var(--global-card-bg-color);
  }

  .mmr-member img,
  .mmr-avatar-placeholder {
    flex: 0 0 5.4rem;
    width: 5.4rem;
    height: 5.4rem;
    border-radius: 50%;
    object-fit: cover;
    background: var(--mmr-blue-soft);
  }

  .mmr-avatar-placeholder {
    display: grid;
    place-items: center;
    color: var(--mmr-blue);
    font-size: 1.15rem;
    font-weight: 700;
  }

  .mmr-member-body h4 {
    margin: 0 0 0.2rem;
    color: var(--global-text-color);
    font-size: 1.05rem;
    font-weight: 700;
  }

  .mmr-member-body h4 a {
    color: inherit;
    text-decoration: none;
  }

  .mmr-member-body h4 a:hover {
    color: var(--mmr-blue);
    text-decoration: underline;
  }

  .mmr-role {
    margin: 0 0 0.45rem;
    color: var(--mmr-blue);
    font-size: 0.9rem;
    font-weight: 700;
  }

  .mmr-bio {
    margin: 0;
    color: var(--global-text-color);
    font-size: 0.9rem;
    line-height: 1.45;
  }

  .mmr-links {
    display: flex;
    flex-wrap: wrap;
    gap: 0.35rem;
    margin-top: 0.55rem;
  }

  .mmr-links a {
    display: inline-flex;
    align-items: center;
    justify-content: center;
    width: 1.7rem;
    height: 1.7rem;
    border: 1px solid rgba(7, 63, 158, 0.35);
    border-radius: 50%;
    color: var(--mmr-blue);
    background: var(--mmr-blue-soft);
    text-decoration: none;
  }

  .mmr-links a:hover {
    border-color: var(--mmr-blue);
    text-decoration: none;
  }

  @media (max-width: 576px) {
    .mmr-news li {
      grid-template-columns: 1fr;
      gap: 0.2rem;
    }

    .mmr-member {
      flex-direction: column;
      min-height: 0;
    }
  }
---

<div class="mmr-lab">
  <section class="mmr-hero">
    <h1>Multimodal Music Research Lab</h1>
    <p class="lead">
      The Multimodal Music Research Lab studies music information retrieval, automatic music transcription, optical music recognition, and their fusion into multimodal musical score retrieval systems. We also explore music theory, musicology, digital music libraries, natural language processing, and expert systems for music understanding.
    </p>
  </section>

  <section class="mmr-section" id="news">
    <h2>News</h2>
    <ul class="mmr-news">
      {% assign mmr_news = site.news | sort: 'date' | reverse %}
      {% for item in mmr_news %}
        <li>
          <time>{{ item.date | date: '%b %d, %Y' }}</time>
          <span>
            {% if item.inline %}
              {{ item.content | remove: '<p>' | remove: '</p>' | emojify }}
            {% else %}
              <a href="{{ item.url | relative_url }}">{{ item.title }}</a>
            {% endif %}
          </span>
        </li>
      {% endfor %}
    </ul>
  </section>

    {% comment %}
      <li>
        <time>July 2026</time>
        <span>One paper was accepted to <a href="https://2026.acmmm.org/">ACMMM 2026</a>.</span>
      </li>
      <li>
        <time>Jan 2026</time>
        <span>One paper was accepted to <a href="https://2026.ieeeicassp.org/">ICASSP 2026</a>.</span>
      </li>
      <li>
        <time>Sep 2025</time>
        <span>Dr. Yaolong Ju presented "Multimedia Music Transcription and its Applications" at <a href="https://www.ascq.org.cn/?p=2308">2025 年全国语音、听觉与音乐声学大会</a>.</span>
      </li>
      <li>
        <time>Sep 2025</time>
        <span>Multiple research positions are open for postdoctoral researchers, senior researchers, research assistants, and students. Please contact us if interested.</span>
      </li>
      <li>
        <time>Aug 2025</time>
        <span>The Multimodal Music Research Lab is recruiting Ph.D. students, master students, and intern/exchange students.</span>
      </li>
      <li>
        <time>Aug 2025</time>
        <span>Dr. Yaolong Ju joined Great Bay University as a tenure-track assistant professor and founded the MMR Lab.</span>
      </li>
    </ul>
  </section>

    {% endcomment %}

  <section class="mmr-section" id="people">
    <h2>Meet the Team</h2>

    <div class="mmr-team-group">
      <h3>Principal Investigator</h3>
      <div class="mmr-team-grid">
        <article class="mmr-member">
          <img src="{{ '/assets/img/prof_pic.jpg' | relative_url }}" alt="Yaolong Ju">
          <div class="mmr-member-body">
            <h4><a href="{{ '/' | relative_url }}">Yaolong Ju</a></h4>
            <p class="mmr-role">Principal Investigator</p>
            <p class="mmr-bio">Tenure-track Assistant Professor at Great Bay University. His research focuses on music information retrieval, automatic music transcription, optical music recognition, and multimodal musical score retrieval.</p>
            <div class="mmr-links" aria-label="Yaolong Ju links">
              <a href="mailto:juyaolong@gbu.edu.cn" aria-label="Email"><i class="fa-solid fa-envelope"></i></a>
              <a href="https://scholar.google.com/citations?user=GHQ0l5YAAAAJ" aria-label="Google Scholar" rel="external nofollow noopener" target="_blank"><i class="ai ai-google-scholar"></i></a>
              <a href="https://github.com/juyaolongpaul" aria-label="GitHub" rel="external nofollow noopener" target="_blank"><i class="fa-brands fa-github"></i></a>
              <a href="https://www.linkedin.com/in/yaolong-ju-06509a5b" aria-label="LinkedIn" rel="external nofollow noopener" target="_blank"><i class="fa-brands fa-linkedin"></i></a>
              <a href="https://dblp.org/pid/215/1921.html" aria-label="DBLP" rel="external nofollow noopener" target="_blank"><i class="ai ai-dblp"></i></a>
            </div>
          </div>
        </article>
      </div>
    </div>

    <div class="mmr-team-group">
      <h3>PostDoc</h3>
      <div class="mmr-team-grid">
        <article class="mmr-member">
          <img src="{{ '/assets/img/mmr-lab/alexandre-dhooge.jpg' | relative_url }}" alt="Alexandre D'Hooge">
          <div class="mmr-member-body">
            <h4><a href="https://adhooge.github.io/" rel="external nofollow noopener" target="_blank">Alexandre D'Hooge</a></h4>
            <p class="mmr-role">PostDoc</p>
            <p class="mmr-bio">Postdoctoral researcher with Dr. Yaolong Ju at Great Bay University. His work focuses on guitar tablature, music practice, composition, and machine learning.</p>
            <div class="mmr-links" aria-label="Alexandre D'Hooge links">
              <a href="mailto:alexandre.dhooge@algomus.fr" aria-label="Email"><i class="fa-solid fa-envelope"></i></a>
              <a href="https://github.com/adhooge" aria-label="GitHub" rel="external nofollow noopener" target="_blank"><i class="fa-brands fa-github"></i></a>
              <a href="https://gitlab.com/adhooge1" aria-label="GitLab" rel="external nofollow noopener" target="_blank"><i class="fa-brands fa-gitlab"></i></a>
              <a href="https://www.linkedin.com/in/alexandre-d-hooge-a5117a156" aria-label="LinkedIn" rel="external nofollow noopener" target="_blank"><i class="fa-brands fa-linkedin"></i></a>
              <a href="https://orcid.org/0000-0003-1634-3406" aria-label="ORCID" rel="external nofollow noopener" target="_blank"><i class="ai ai-orcid"></i></a>
              <a href="https://scholar.google.com/citations?user=aWrwV9IAAAAJ" aria-label="Google Scholar" rel="external nofollow noopener" target="_blank"><i class="ai ai-google-scholar"></i></a>
            </div>
          </div>
        </article>
      </div>
    </div>

    <div class="mmr-team-group">
      <h3>PhD Students</h3>
      <div class="mmr-team-grid">
        <article class="mmr-member">
          <div class="mmr-avatar-placeholder" aria-hidden="true">YP</div>
          <div class="mmr-member-body">
            <h4><a href="https://scholar.google.com/citations?user=haXxXAIAAAAJ&hl=en" rel="external nofollow noopener" target="_blank">Yizhao Peng</a></h4>
            <p class="mmr-role">PhD Student</p>
            <p class="mmr-bio">Research interests include music information retrieval, signal processing, computer vision, and AI for audio/music understanding.</p>
            <div class="mmr-links" aria-label="Yizhao Peng links">
              <a href="https://scholar.google.com/citations?user=haXxXAIAAAAJ&hl=en" aria-label="Google Scholar" rel="external nofollow noopener" target="_blank"><i class="ai ai-google-scholar"></i></a>
            </div>
          </div>
        </article>
      </div>
    </div>

    <div class="mmr-team-group">
      <h3>Master Students</h3>
      <div class="mmr-team-grid">
        <article class="mmr-member">
          <img src="{{ '/assets/img/mmr-lab/chengshuai-liang.jpg' | relative_url }}" alt="Chengshuai Liang">
          <div class="mmr-member-body">
            <h4>Chengshuai Liang</h4>
            <p class="mmr-role">Master Student</p>
            <p class="mmr-bio">My name is Chengshuai Liang. I recently completed my undergraduate studies and am currently a graduate student in Artificial Intelligence. My current research focuses on music classification, and I am interested in applying machine learning and AI techniques to music understanding and audio analysis.</p>
          </div>
        </article>

        <article class="mmr-member">
          <img src="{{ '/assets/img/mmr-lab/xinwei_jiang.jpg' | relative_url }}" alt="Xinwei Jiang">
          <div class="mmr-member-body">
            <h4><a href="https://jiangbing22.github.io/jingbing22.github.io/" rel="external nofollow noopener" target="_blank">Xinwei Jiang</a></h4>
            <p class="mmr-role">Master Student</p>
            <p class="mmr-bio">My research focuses on music information retrieval and multimodal intelligence, with interests in singing and music audio understanding, affective computing, and cross-modal representation learning.</p>
            <div class="mmr-links" aria-label="Xinwei Jiang links">
              <a href="mailto:505139705@qq.com" aria-label="Email"><i class="fa-solid fa-envelope"></i></a>
              <a href="https://github.com/jiangbing22?tab=repositories" aria-label="GitHub" rel="external nofollow noopener" target="_blank"><i class="fa-brands fa-github"></i></a>
            </div>
          </div>
        </article>

        <article class="mmr-member">
          <div class="mmr-avatar-placeholder" aria-hidden="true">MS</div>
          <div class="mmr-member-body">
            <h4>Open Master Position</h4>
            <p class="mmr-role">Master Student</p>
            <p class="mmr-bio">To be announced.</p>
          </div>
        </article>
      </div>
    </div>

    <div class="mmr-team-group">
      <h3>Administrative Assistant</h3>
      <div class="mmr-team-grid">
        <article class="mmr-member">
          <div class="mmr-avatar-placeholder" aria-hidden="true">蔡</div>
          <div class="mmr-member-body">
            <h4>蔡芳婷</h4>
            <p class="mmr-role">Administrative Assistant</p>
          </div>
        </article>
      </div>
    </div>
  </section>
</div>
