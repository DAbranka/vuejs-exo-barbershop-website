<template>
  <div>
    <section>
      <article>
        <div>
          <!-- <div><img src="" alt="icon/png" /></div> -->
          <a href="#hero">The Gentlemen's Cut</a>
        </div>
        <div>
          <p>Premium grooming for the modern gentleman</p>
        </div>
      </article>

      <article>
        <p>Hours</p>
        <ul>
          <li>Mon-Fri: 9am - 7pm</li>
          <li>Sat: 10am - 5pm</li>
          <li>Sun: Closed</li>
        </ul>
      </article>

      <article>
        <p>Contact</p>
        <ul>
          <li>456 Oak Avenue</li>
          <li>Downtown, NY 10002</li>
          <li>(555) 987-6543</li>
        </ul>
      </article>
    </section>
    <section>
      <p>
        © 2026
        <a
          :style="{
            textDecoration: 'none',
          }"
          href="https://cryptidcrowd.studio/"
          target="_blank"
          rel="noopener noreferrer"
          >CryptidCrowd</a
        >. All rights reserved.
      </p>
    </section>
  </div>
</template>

<style scoped>
section:first-child {
  display: flex;
  padding: 2.5rem 0 1.5rem 0;
  gap: 2rem;
  border-top: 1px solid hsl(from var(--white-color) h s 45 / 0.5);
  border-bottom: 1px solid hsl(from var(--white-color) h s 45 / 0.2);
}

article {
  flex: 1;
  padding: 0 1rem;
}

section:last-child {
  text-align: center;
  padding: 2rem;
  font-size: 0.9rem;
  color: hsl(from var(--white-color) h s 60 / 1);
}
section:last-child a {
  color: var(--white-color);
  font-weight: 600;
  transition: color 0.3s ease;
}

section:last-child a:hover {
  text-decoration: none;
  color: var(--accent);
}

article:first-child div:first-child a {
  font-weight: 600;
  text-decoration: none;
  color: hsl(var(--white-color) / 1);
}

article:first-child div:first-child a:hover {
  color: var(--accent);
  transition: color 0.3s ease;
}

article:first-child div:first-child {
  display: flex;
  align-items: center;
  gap: 1rem;
}

article:first-child div:last-child p {
  margin-top: 1rem;
  font-size: 0.9rem;
  color: hsl(from var(--white-color) h s 70 / 1);
}

article:nth-child(2) p,
article:nth-child(3) p {
  font-weight: bold;
}

article:nth-child(2) ul,
article:nth-child(3) ul {
  font-size: 0.9rem;
  color: hsl(from var(--white-color) h s 70 / 1);
  line-height: 1.3;
}

ul {
  list-style: none;
  margin-top: 1rem;
}
</style>
