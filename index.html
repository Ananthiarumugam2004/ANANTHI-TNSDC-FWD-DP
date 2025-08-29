const prefersReduced = window.matchMedia('(prefers-reduced-motion: reduce)').matches;
const root = document.documentElement;
const navWrap = document.getElementById('navWrap');
const progress = document.getElementById('progress');
const themeBtns = [document.getElementById('toggleTheme'), document.getElementById('toggleThemeMobile')];
const animBtns = [document.getElementById('toggleAnim'), document.getElementById('toggleAnimMobile')];
const links = [...document.querySelectorAll('.menu a[href^="#"]')];
const sections = links.map(a => document.querySelector(a.getAttribute('href'))).filter(Boolean);

document.getElementById('year').textContent = new Date().getFullYear();

const THEME_KEY = 'fp-theme';
function applyTheme(theme) {
  if (theme === 'dark') {
    root.classList.add('dark');
    setPressed(themeBtns, true);
  } else {
    root.classList.remove('dark');
    setPressed(themeBtns, false);
  }
  localStorage.setItem(THEME_KEY, theme);
}
function setPressed(btns, pressed) {
  btns.forEach(b => { if (b) b.setAttribute('aria-pressed', String(pressed)); });
}
const saved = localStorage.getItem(THEME_KEY) || (window.matchMedia('(prefers-color-scheme: dark)').matches ? 'dark' : 'light');
applyTheme(saved);
themeBtns.forEach(btn => btn && btn.addEventListener('click', () => {
  applyTheme(root.classList.contains('dark') ? 'light' : 'dark');
}));

const ANIM_KEY = 'fp-anim';
function setAnim(on) {
  if (prefersReduced) on = false;
  navWrap.classList.toggle('animate', on);
  setPressed(animBtns, on);
  localStorage.setItem(ANIM_KEY, on ? 'on' : 'off');
}
const savedAnim = localStorage.getItem(ANIM_KEY);
setAnim(savedAnim ? savedAnim === 'on' : true);
animBtns.forEach(btn => btn && btn.addEventListener('click', () => setAnim(!navWrap.classList.contains('animate'))));

function updateProgress() {
  const h = document.documentElement;
  const scrollTop = h.scrollTop || document.body.scrollTop;
  const docHeight = h.scrollHeight - h.clientHeight;
  const pct = docHeight > 0 ? (scrollTop / docHeight) * 100 : 0;
  progress.style.width = pct + '%';
}
document.addEventListener('scroll', updateProgress, { passive: true });
updateProgress();

const spy = new IntersectionObserver((entries) => {
  entries.forEach(entry => {
    const id =