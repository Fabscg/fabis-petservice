<template>
    <div class="page">
  
      <!-- HEADER -->
      <header class="header">
        <div class="paws-row">
          <PawIcon v-for="n in 3" :key="n" class="paw-svg" />
        </div>
        <h1>Furry Paws TO</h1>
        <div class="role-badge">Dog Walking &amp; Pet Sitting Services · Toronto Midtown</div>
        <div class="cred-row">
          <span class="cred">✓ Pet First Aid Certified</span>
          <span class="cred">✓ Fully Insured</span>
          <span class="cred">✓ Free Meet &amp; Greet</span>
        </div>
      </header>
  
      <!-- MEET & GREET BAR -->
      <div class="meet-greet-bar">
        <div class="mg-title">✓ Free meet &amp; greet included</div>
        <div class="mg-sub">No obligation — let's get acquainted before we start</div>
      </div>
  
      <!-- CTA BAR -->
      <div class="cta-bar">
        <a href="tel:6478234713" class="cta-btn">
          <PhoneIcon /> Call now
        </a>
        <a href="mailto:info@furrypawstoronto.ca" class="cta-btn outline">
          <MailIcon /> Email us
        </a>
      </div>
  
      <!-- SERVICES SECTION -->
      <section>
        <h2>Services &amp; pricing</h2>
  
        <div class="meet-greet-card">
          <div class="mg-icon">
            <UsersIcon />
          </div>
          <div>
            <div class="mg-card-title">Free meet &amp; greet</div>
            <div class="mg-desc">Before we start, I come to you for a relaxed, no-obligation visit. Your pet and I get to know each other, we go over routines and preferences, and you can ask me anything. It's the best way to make sure it's a great fit.</div>
          </div>
        </div>
  
        <div class="section-label label-dog">🐾 Dog services</div>
        <div class="services-grid">
          <ServiceCard
            v-for="service in dogServices"
            :key="service.name"
            :service="service"
            type="dog"
          />
        </div>
  
        <div class="section-label label-cat">🐱 Cat services</div>
        <div class="services-grid">
          <ServiceCard
            v-for="service in catServices"
            :key="service.name"
            :service="service"
            type="cat"
          />
        </div>
      </section>
  
      <!-- WHY SECTION -->
      <section class="no-top">
        <h2>Why choose Furry Paws TO?</h2>
        <ul class="why-list">
          <li v-for="reason in reasons" :key="reason">
            <div class="why-dot">
              <CheckIcon />
            </div>
            <span>{{ reason }}</span>
          </li>
        </ul>
      </section>
  
      <!-- CONTACT SECTION -->
      <section class="no-top">
        <div class="contact-card">
          <h2>Get in touch</h2>
          <br />
          <div class="contact-row">
            <div class="c-icon"><PhoneIconOrange /></div>
            <div>
              <div class="c-label">Phone</div>
              <a href="tel:6478234713" class="c-link c-value">647-823-4713</a>
            </div>
          </div>
          <div class="contact-row">
            <div class="c-icon"><MailIconOrange /></div>
            <div>
              <div class="c-label">Email</div>
              <a href="mailto:info@furrypawstoronto.ca" class="c-link c-value">info@furrypawstoronto.ca</a>
            </div>
          </div>
          <div class="contact-row">
            <div class="c-icon"><InstagramIcon /></div>
            <div>
              <div class="c-label">Instagram</div>
              <a href="https://www.instagram.com/furrypawsto/" class="c-link c-value">@FurryPawsTO</a>
            </div>
          </div>
        </div>
      </section>
  
      <!-- FOOTER -->
      <footer>
        <div class="footer-paws">
          <PawIcon v-for="n in 3" :key="n" class="footer-paw" />
        </div>
        Furry Paws TO &middot; Dog Walking &amp; Pet Sitting &middot; Toronto Midtown, ON
      </footer>
  
    </div>
  </template>
  
  <script setup>
  // ─── Data ────────────────────────────────────────────────────────────────────
  
  const dogServices = [
    {
      icon: '🦮',
      name: 'Solo walk',
      desc: 'One-on-one, full attention, tailored pace — just for your dog.',
      prices: ['$25 / 30 min', '$33 / 45 min'],
    },
    {
      icon: '🐕🐕',
      name: 'Semi-private walk',
      desc: 'Small group of 2–3 dogs — social, fun, and more affordable.',
      prices: ['$18 / 30 min', '$25 / 45 min'],
    },
    {
      icon: '🏠',
      name: 'Dog drop-in visit',
      desc: 'Home check-in for feeding, play time, and potty breaks.',
      prices: ['$20 / 30 min', '$28 / 45 min'],
    },
  ]
  
  const catServices = [
    {
      icon: '🐈',
      name: 'Cat drop-in visit',
      desc: 'Feeding, fresh water, litter scooping, play, and cuddles while you\'re away.',
      prices: ['$18 / 30 min', '$25 / 45 min'],
    },
  ]
  
  const reasons = [
    "Pet First Aid certified — your pet's safety comes first",
    'Fully insured for your peace of mind',
    'Free meet & greet so your pet is comfortable from day one',
    'Photo updates sent after every walk or visit',
    'Serving Toronto Midtown pet families with genuine love and care',
  ]
  </script>
  
  <script>
  // ─── Sub-components defined inline ───────────────────────────────────────────
  
  const PawIcon = {
    template: `<svg viewBox="0 0 30 30" fill="#3A2000" style="width:22px;height:22px;opacity:0.5">
      <ellipse cx="15" cy="22" rx="8" ry="6"/>
      <ellipse cx="7" cy="14" rx="4" ry="5"/>
      <ellipse cx="23" cy="14" rx="4" ry="5"/>
      <ellipse cx="11" cy="8" rx="3.5" ry="4"/>
      <ellipse cx="19" cy="8" rx="3.5" ry="4"/>
    </svg>`
  }
  
  const PhoneIcon = {
    template: `<svg width="16" height="16" viewBox="0 0 16 16" fill="none" stroke="#3A2000" stroke-width="2">
      <path d="M3 2h3l1.5 3.5L6 7s1 2 3 3l1.5-1.5L14 10v3c-8 1-12-6-11-11z"/>
    </svg>`
  }
  
  const MailIcon = {
    template: `<svg width="16" height="16" viewBox="0 0 16 16" fill="none" stroke="#F9A825" stroke-width="2">
      <rect x="2" y="3" width="12" height="10" rx="1"/>
      <path d="M2 3l6 5 6-5"/>
    </svg>`
  }
  
  const UsersIcon = {
    template: `<svg width="22" height="22" viewBox="0 0 24 24" fill="none" stroke="#fff" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
      <path d="M17 21v-2a4 4 0 0 0-4-4H5a4 4 0 0 0-4 4v2"/>
      <circle cx="9" cy="7" r="4"/>
      <path d="M23 21v-2a4 4 0 0 0-3-3.87"/>
      <path d="M16 3.13a4 4 0 0 1 0 7.75"/>
    </svg>`
  }
  
  const CheckIcon = {
    template: `<svg viewBox="0 0 12 12" fill="none" stroke="#3A2000" stroke-width="2" style="width:12px;height:12px">
      <polyline points="2,6 5,9 10,3"/>
    </svg>`
  }
  
  const PhoneIconOrange = {
    template: `<svg width="18" height="18" viewBox="0 0 16 16" fill="none" stroke="#F9A825" stroke-width="1.8">
      <path d="M3 2h3l1.5 3.5L6 7s1 2 3 3l1.5-1.5L14 10v3c-8 1-12-6-11-11z"/>
    </svg>`
  }
  
  const MailIconOrange = {
    template: `<svg width="18" height="18" viewBox="0 0 16 16" fill="none" stroke="#F9A825" stroke-width="1.8">
      <rect x="2" y="3" width="12" height="10" rx="1"/>
      <path d="M2 3l6 5 6-5"/>
    </svg>`
  }
  
  const InstagramIcon = {
    template: `<svg width="18" height="18" viewBox="0 0 16 16" fill="none" stroke="#F9A825" stroke-width="1.8">
      <rect x="2" y="2" width="12" height="12" rx="3"/>
      <circle cx="8" cy="8" r="3"/>
      <circle cx="11.5" cy="4.5" r="0.5" fill="#F9A825"/>
    </svg>`
  }
  
  const ServiceCard = {
    props: ['service', 'type'],
    template: `
      <div :class="['service-card', type === 'cat' ? 'cat' : '']">
        <div class="service-icon">{{ service.icon }}</div>
        <div class="service-name">{{ service.name }}</div>
        <div class="service-desc">{{ service.desc }}</div>
        <div class="price-row">
          <span v-for="price in service.prices" :key="price" :class="['price-pill', type]">{{ price }}</span>
        </div>
      </div>
    `
  }
  
  export default {
    components: {
      PawIcon, PhoneIcon, MailIcon, UsersIcon, CheckIcon,
      PhoneIconOrange, MailIconOrange, InstagramIcon, ServiceCard
    }
  }
  </script>
  
  <style scoped>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
  
  .page { font-family: 'Nunito', sans-serif; background: #FFF8F0; color: #3A2000; }
  
  /* Header */
  .header { background: #F9A825; padding: 48px 24px 32px; text-align: center; }
  .paws-row { display: flex; justify-content: center; gap: 10px; margin-bottom: 12px; }
  h1 { font-family: 'Fredoka One', sans-serif; font-size: clamp(32px, 7vw, 48px); color: #3A2000; line-height: 1.1; }
  .role-badge { display: inline-block; background: #FFD54F; color: #7A4800; font-size: 12px; font-weight: 800; letter-spacing: 1.5px; text-transform: uppercase; padding: 5px 16px; border-radius: 20px; margin: 10px 0 14px; }
  .cred-row { display: flex; flex-wrap: wrap; justify-content: center; gap: 8px; margin-bottom: 4px; }
  .cred { background: #fff; color: #7A4800; font-size: 11px; font-weight: 800; padding: 4px 12px; border-radius: 20px; border: 1.5px solid #F0C080; }
  
  /* Meet & Greet bar */
  .meet-greet-bar { background: #1D9E75; padding: 14px 24px; text-align: center; }
  .mg-title { font-size: 16px; font-weight: 800; color: #E1F5EE; margin-bottom: 3px; }
  .mg-sub { font-size: 12px; color: #9FE1CB; font-weight: 600; }
  
  /* CTA bar */
  .cta-bar { background: #3A2000; padding: 18px 24px; text-align: center; display: flex; flex-wrap: wrap; gap: 12px; justify-content: center; }
  .cta-btn { display: inline-flex; align-items: center; gap: 8px; background: #F9A825; color: #3A2000; font-family: 'Nunito', sans-serif; font-weight: 800; font-size: 15px; text-decoration: none; padding: 12px 22px; border-radius: 30px; border: none; cursor: pointer; transition: background 0.2s; }
  .cta-btn:hover { background: #FFD54F; }
  .cta-btn.outline { background: transparent; color: #F9A825; border: 2px solid #F9A825; }
  .cta-btn.outline:hover { background: #F9A825; color: #3A2000; }
  
  /* Sections */
  section { max-width: 640px; margin: 0 auto; padding: 40px 24px; }
  section.no-top { padding-top: 0; }
  h2 { font-family: 'Fredoka One', sans-serif; font-size: 26px; color: #3A2000; margin-bottom: 20px; }
  
  /* Section labels */
  .section-label { display: inline-flex; align-items: center; gap: 8px; font-size: 13px; font-weight: 800; letter-spacing: 1.5px; text-transform: uppercase; padding: 5px 14px; border-radius: 20px; margin-bottom: 16px; }
  .label-dog { background: #FFF3E0; color: #7A4800; }
  .label-cat { background: #FCE4EC; color: #880E4F; }
  
  /* Services grid */
  .services-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(170px, 1fr)); gap: 14px; margin-bottom: 28px; }
  .service-card { background: #fff; border: 2px solid #F0C080; border-radius: 14px; padding: 18px 16px; }
  .service-card.cat { border-color: #F48FB1; }
  .service-icon { font-size: 28px; margin-bottom: 8px; }
  .service-name { font-weight: 800; font-size: 15px; color: #3A2000; margin-bottom: 4px; }
  .service-desc { font-size: 12px; color: #7A5820; line-height: 1.5; margin-bottom: 10px; }
  .price-row { display: flex; gap: 8px; flex-wrap: wrap; }
  .price-pill { font-size: 11px; font-weight: 800; padding: 3px 10px; border-radius: 8px; }
  .price-pill.dog { background: #FFF3E0; color: #7A4800; border: 1.5px solid #F9A825; }
  .price-pill.cat { background: #FCE4EC; color: #880E4F; border: 1.5px solid #F48FB1; }
  
  /* Meet & greet card */
  .meet-greet-card { background: #E1F5EE; border: 2px solid #5DCAA5; border-radius: 14px; padding: 20px 22px; display: flex; align-items: flex-start; gap: 16px; margin-bottom: 28px; }
  .mg-icon { width: 44px; height: 44px; background: #1D9E75; border-radius: 50%; display: flex; align-items: center; justify-content: center; flex-shrink: 0; }
  .mg-card-title { font-weight: 800; font-size: 16px; color: #085041; margin-bottom: 4px; }
  .mg-desc { font-size: 13px; color: #0F6E56; line-height: 1.6; }
  
  /* Why list */
  .why-list { list-style: none; display: flex; flex-direction: column; gap: 12px; }
  .why-list li { display: flex; align-items: flex-start; gap: 12px; font-size: 15px; color: #3A2000; line-height: 1.5; }
  .why-dot { width: 22px; height: 22px; background: #F9A825; border-radius: 50%; flex-shrink: 0; margin-top: 2px; display: flex; align-items: center; justify-content: center; }
  
  /* Contact card */
  .contact-card { background: #F9A825; border-radius: 18px; padding: 28px 24px; }
  .contact-card h2 { color: #3A2000; }
  .contact-row { display: flex; align-items: center; gap: 12px; margin-bottom: 12px; }
  .c-icon { width: 40px; height: 40px; background: #fff; border-radius: 50%; display: flex; align-items: center; justify-content: center; flex-shrink: 0; }
  .c-label { font-size: 11px; color: #7A4800; font-weight: 700; text-transform: uppercase; letter-spacing: 1px; }
  .c-value { font-size: 15px; font-weight: 800; color: #3A2000; }
  .c-link { color: #3A2000; text-decoration: none; }
  .c-link:hover { text-decoration: underline; }
  
  /* Footer */
  footer { background: #3A2000; color: #F0C080; text-align: center; padding: 20px 24px; font-size: 13px; }
  .footer-paws { display: flex; justify-content: center; gap: 8px; margin-bottom: 8px; opacity: 0.4; }
  </style>
  