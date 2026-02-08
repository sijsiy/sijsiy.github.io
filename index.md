<style>
/* Home 2-column layout */
.home-hero{
  display:flex;
  gap:24px;
  align-items:flex-start;
  justify-content:space-between;
  flex-wrap:wrap;
  margin-top: 12px;
  margin-bottom: 24px;
}

.home-left{
  flex: 0 0 180px;   /* 왼쪽 컬럼 폭 */
}

.home-right{
  flex: 1 1 360px;   /* 오른쪽 설명 영역 */
  min-width: 280px;
}

/* Profile image cutout */
.profile-wrap{ display:inline-block; position:relative; }
.profile-img{
  width: 160px;     /* “왼쪽에 작게” */
  height:auto;
  display:block;
  filter: drop-shadow(0 10px 22px rgba(0,0,0,0.18));
}
.profile-wrap::after{
  content:"";
  position:absolute;
  inset:0;
  z-index:-1;
  filter: blur(14px);
  opacity:0.22;
}

/* Right text styling */
.home-name{
  margin: 0 0 6px 0;
  line-height: 1.2;
}
.home-tagline{
  margin: 0 0 10px 0;
}
.home-meta{
  margin: 0 0 12px 0;
  padding-left: 18px;
}

/* Mobile: stack */
@media (max-width: 720px){
  .home-left{ flex: 0 0 100%; }
  .profile-img{ width: 140px; }
}
</style>

<div class="home-hero">
  <div class="home-left">
    <div class="profile-wrap">
      <img src="{{ '/profile.png' | relative_url }}" class="profile-img" alt="Profile photo">
    </div>
  </div>

  <div class="home-right">
    <h1 class="home-name">Sijeoung Kim</h1>
    <p class="home-tagline"><strong>Research Professor</strong>, Korea University</p>

    <ul class="home-meta">
      <li>Research: Digital Government, Privacy, Digital Administrative Burden</li>
      <li>Teaching: AI-embedded PBL / STS-informed learning design</li>
      <li>Methods: survey/experiments, panel data, mixed methods</li>
    </ul>

    <p>
      I study how people experience digital public services—especially privacy concerns, trust, and administrative burden—
      and how we can design better public services and learning experiences.
    </p>

    <p>
      <a href="{{ '/cv.html' | relative_url }}">CV</a> ·
      <a href="{{ '/publications.html' | relative_url }}">Publications</a> ·
      <a href="{{ '/projects.html' | relative_url }}">Projects</a>
    </p>
  </div>
</div>
