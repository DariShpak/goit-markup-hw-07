:root {
  --primary-color: #4d5ae5;
  --pressed-state-color: #404bbf;
  --heading-text-color: #2e2f42;
  --main-text-color: #434455;
  --subtle-text-color: #8e8f99;
  --accent-color: #e7e9fc;
  --light-mode-color: #f4f4fd;
  --hero-section-color: #ffffff;
  --success-color: #31d0aa;
  --hero-bg: linear-gradient(rgba(46, 47, 66, 0.7), rgba(46, 47, 66, 0.7));
  --transition-value: 250ms cubic-bezier(0.4, 0, 0.2, 1);
}

body {
  font-family: "Roboto", "Raleway", sans-serif;
  font-weight: 400;
  font-size: 16px;
  letter-spacing: 0.02em;
  color: var(--main-text-color);
  background-color: var(--hero-section-color);
}

.is-hidden {
  opacity: 0;
  visibility: hidden;
  pointer-events: none;
}

.no-scroll {
  overflow: hidden;
}

.container {
  margin-left: auto;
  margin-right: auto;
  max-width: 428px;
  padding-left: 16px;
  padding-right: 16px;
}

.section {
  padding-top: 96px;
  padding-bottom: 96px;
}

.visually-hidden {
  position: absolute;
  width: 1px;
  height: 1px;
  margin: -1px;
  border: 0;
  padding: 0;
  white-space: nowrap;
  clip-path: inset(100%);
  clip: rect(0 0 0 0);
  overflow: hidden;
}

.list {
  list-style: none;
}

.link {
  text-decoration: none;
}

.link:visited {
  color: var(--heading-text-color);
}

button {
  cursor: pointer;
}

h1,
h2,
h3,
p {
  margin-top: 0;
  margin-bottom: 0;
}

ul,
ol {
  margin-top: 0;
  margin-bottom: 0;
  padding-left: 0;
}

img {
  display: block;
  max-width: 100%;
  height: auto;

}

.section-title {
  margin-left: auto;
  margin-right: auto;
  margin-bottom: 72px;

  color: var(--heading-text-color);

  font-size: 36px;
  font-weight: 700;
  line-height: calc(40 / 36);
  text-transform: capitalize;
  text-align: center;
}

.section-subtitle {
  color: var(--heading-text-color);

  font-weight: 500;
  font-size: 20px;

  line-height: calc(24 / 20);

  margin-bottom: 8px;
}

.section-text {
  color: var(--main-text-color);
  line-height: calc(24 / 16);
}

.desc-wrapper {
  text-align: center;
  padding-top: 32px;
  padding-bottom: 32px;
  padding-left: 16px;
  padding-right: 16px;
}

/* ---------------HEADER---------------- */

.header {
  padding-top: 24px;
  padding-bottom: 24px;
  background-color: var(--hero-section-color);
  border-bottom: 1px solid var(--accent-color);
}

.header-container {
  display: flex;
  justify-content: space-between;
}

@media screen and (max-width: 767px) {
  .nav-list {
    display: none;
  }

  .address {
    display: none;
  }
}

/* header logotype */

.logo {
  font-family: "Raleway", sans-serif;
  font-weight: 800;
  font-size: 18px;
  line-height: 1.3;
  letter-spacing: 0.03em;
  text-transform: uppercase;
  text-decoration: none;
}

.logo .accent {
  color: var(--primary-color);
}

.logo-header {
  color: var(--heading-text-color);
}

/* ----------------MOBILE-MENU-OPEN---------------- */

.mob-menu-open {
  background-color: transparent;
  border: none;
  padding: 0;
  line-height: 0;
}

.mob-menu-icon {
  justify-content: center;
  stroke-width: 0;
  stroke: var(--heading-text-color);
  fill: var(--heading-text-color);
}

/* ---------------MOBILE-MENU---------------- */

.mob-menu {
  position: fixed;
  width: 100%;
  height: 100%;
  top: 0;
  left: 0;

  background-color: var(--hero-section-color);
}

.mob-menu .container {
  height: 100%;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  padding: 40px;
}

.mob-menu-close {
  display: flex;
  justify-content: center;
  align-items: center;

  margin-left: auto;
  margin-bottom: 16px;

  width: 24px;
  height: 24px;
  border-radius: 50%;

  background: var(--accent-color);
  border: 1px solid rgba(0, 0, 0, 0.1);

  transition: background-color var(--transition-value),
    border-color var(--transition-value), fill var(--transition-value);
}

.mob-menu-close:is(:hover, :focus) {
  background-color: var(--pressed-state-color);
  border-color: var(--pressed-state-color);
  fill: var(--hero-section-color);
}

.mob-menu-nav .link.current {
  color: var(--pressed-state-color);
}

.mob-menu-nav-item:not(:last-child) {
  margin-bottom: 40px;
}

.mob-menu-nav-item .section-title {
  font-weight: 700;
}

.address-link-tel {
  font-style: normal;
  font-weight: 600;
  font-size: 24px;
  text-transform: capitalize;
  font-weight: 600;
  line-height: calc(40 / 36);
  color: var(--primary-color);
}

.address-link-mail {
  font-style: normal;
  font-weight: 500;
  font-size: 20px;
  line-height: calc(24 / 20);
  color: var(--main-text-color);
}

.mob-menu-item:not(:last-child) {
  margin-bottom: 40px;
}

.socials-list {
  width: 100%;
  margin-top: 48px;
  display: flex;
  gap: 26px;
  flex-basis: calc((100% - 168px) / 3);
}

@media screen and (min-width: 428px) {
  .address-link-tel {
    font-size: 36px;
  }

  .socials-list {
    gap: 56px;
  }
}

.socials-item {
  width: 40px;
  height: 40px;
}

.socials-item-link {
  width: 100%;
  height: 100%;
  background-color: var(--primary-color);
  display: flex;
  align-items: center;
  justify-content: center;
  border-radius: 50%;

  transition: background-color var(--transition-value);
}

.socials-item-link:is(:hover, :focus) {
  background-color: var(--pressed-state-color);
}

.socials-icon {
  fill: var(--light-mode-color);
}

/* ---------------HERO-SECTION-------------- */

.hero-section {
  padding-top: 112px;
  padding-bottom: 112px;

  margin-right: auto;
  margin-left: auto;
  max-width: 428px;
  height: 432px;
  background-image: var(--hero-bg), url(../images/hero/hero-bg-mob.jpg);
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
}

@media (min-device-pixel-ratio: 2),
  (min-resolution: 192dpi),
  (min-resolution: 2dppx) {
  .hero-section {
    background-image: var(--hero-bg), url("../images/hero/hero-bg-mob@2x.jpg");
  }
}

.hero-title {
  margin-left: auto;
  margin-right: auto;
  margin-bottom: 72px;
  max-width: 318px;

  color: var(--hero-section-color);

  text-align: center;
  font-weight: 700;
  font-size: 32px;
  line-height: calc(36 / 40);
}

@media screen and (min-width: 343px) {
  .hero-title {
    font-size: 36px;
  }
}

.hero-btn {
  display: block;
  margin-right: auto;
  margin-left: auto;

  padding-top: 16px;
  padding-right: 32px;
  padding-bottom: 16px;
  padding-left: 32px;
  border: 1px transparent;
  border-radius: 4px;

  font-weight: 500;
  line-height: 1.5;
  background-color: var(--primary-color);
  box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.15);
  color: var(--hero-section-color);
  letter-spacing: 0.04em;

  transition: background-color var(--transition-value);
}

.hero-btn:hover,
.hero-btn:focus {
  background-color: var(--pressed-state-color);
}

/* --------------- FEAUTERS-SECTION -------------- */

.feauters-img {
  display: none;
}

.feauters-list {
  display: flex;
  flex-direction: column;
  gap: 72px;
}

.feauters-item .section-title {
  margin-bottom: 8px;
}

/* -----------------SERVICES ---------------- */
.services-section {
  display: none;
}

/* --------------- OUR TEAM ---------------- */

.team-section {
  padding-bottom: 128px;

  background-color: var(--light-mode-color);
}

.team-card {
  margin-left: auto;
  margin-right: auto;

  max-width: 264px;
  background-color: var(--hero-section-color);
  box-shadow: 0px 1px 6px rgba(46, 47, 66, 0.08),
    0px 1px 1px rgba(46, 47, 66, 0.16), 0px 2px 1px rgba(46, 47, 66, 0.08);
  border-radius: 0px 0px 4px 4px;
}

.team-card:not(:first-child) {
  margin-top: 72px;
}

.socials-list {
  margin-top: 8px;

  display: flex;
  justify-content: center;
  gap: 24px;
}

.socials-item {
  width: 40px;
  height: 40px;
}

.socials-item-link {
  width: 100%;
  height: 100%;
  background-color: var(--primary-color);
  display: flex;
  align-items: center;
  justify-content: center;
  border-radius: 50%;

  transition: background-color var(--transition-value);
}

.socials-item-link:is(:hover, :focus) {
  background-color: var(--pressed-state-color);
}

.socials-icon {
  fill: var(--light-mode-color);
}

/* ------------------CUSTOMERS----------------- */

.customers-list {
  display: flex;
  flex-wrap: wrap;
  column-gap: 16px;
  row-gap: 72px;
}

.customers-item {
  flex-basis: calc((100% - 16px) / 2);
  max-width: 190px;

  height: 88px;
}

.customers-link {
  width: 100%;
  height: 100%;
  display: flex;
  align-items: center;
  justify-content: center;

  color: var(--subtle-text-color);
  border: 1px solid var(--subtle-text-color);
  border-radius: 4px;

  transition: color var(--transition-value),
    border-color var(--transition-value);
}

.customers-link:visited {
  color: var(--subtle-text-color);
}

.customers-icon {
  fill: currentColor;
}

.customers-link:is(:hover, :focus) {
  border-color: var(--pressed-state-color);
  color: var(--pressed-state-color);
}

/* -----------------FOOTER------------------- */

.footer {
  background-color: var(--heading-text-color);
  color: var(--accent-color);
}

.footer-content-wrapper {
  margin-left: auto;
  margin-right: auto;

  max-width: 268px;

  text-align: center;
}

.logo.footer {
  color: var(--light-mode-color);
}

.footer-text {
  margin-top: 16px;
  color: inherit;
}

.footer-socials {
  text-align: center;
}

.footer-socials .section-subtitle {
  color: var(--hero-section-color);
  font-size: 16px;

  margin-top: 72px;
}

.footer-socials .socials-list {
  margin-top: 16px;
  padding-left: 0;
  padding-right: 0;
  gap: 16px;
}

.footer-socials .socials-item-link {
  background: rgba(255, 255, 255, 0.1);
  transition: background-color var(--transition-value);
}

.footer-socials .socials-item-link:is(:hover, :focus) {
  background: var(--success-color);
}

.email-input {
  width: 100%;
  text-align: center;
}

.email-input .section-subtitle {
  color: var(--hero-section-color);
  font-size: 16px;
  margin-bottom: 16px;
  margin-top: 72px;
}

.input-wrapper {
  display: block;
}

.form-input {
  display: flex;
  width: 100%;
  height: 40px;
  background-color: transparent;
  border: 1px solid rgba(255, 255, 255, 0.3);
  filter: drop-shadow(0px 4px 4px rgba(0, 0, 0, 0.15));
  border-radius: 4px;
  font-size: 12px;
  color: var(--hero-section-color);
  outline: transparent;
  padding-left: 16px;
  transition: border-color var(--transition-value);
}

.form-input::placeholder {
  padding-top: 8px;
  padding-bottom: 8px;

  font-size: 12px;
  line-height: 2;
  display: flex;
  align-items: center;
  letter-spacing: 0.04em;
  color: rgba(255, 255, 255, 0.6);
}

.form-input:focus {
  border-color: var(--primary-color);
}

.form-btn.footer {
  margin-top: 16px;
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  padding: 8px 24px;
  gap: 16px;
}

.send-icon {
  fill: var(--hero-section-color);
}

/* ------------------------MODAL------------------- */

.backdrop {
  position: fixed;
  top: 0;

  width: 100%;
  height: 100%;

  background-color: rgba(46, 47, 66, 0.4);

  transition: opacity var(--transition-value),
    visibility var(--transition-value);
}

.modal {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);

  padding-top: 24px;
  padding-bottom: 24px;
  padding-left: 16px;
  padding-right: 16px;

  background: #fcfcfc;
  box-shadow: 0px 1px 1px rgba(0, 0, 0, 0.14), 0px 1px 3px rgba(0, 0, 0, 0.12),
    0px 2px 1px rgba(0, 0, 0, 0.2);
  border-radius: 4px;

  transition: transform var(--transition-value);
}

.backdrop.is-hidden .modal {
  transform: translate(-50%, -50%) scale (0);
}

.modal-close {
  position: absolute;
  top: 12px;
  right: 12px;

  display: flex;
  align-items: center;
  justify-content: center;

  width: 24px;
  height: 24px;
  border-radius: 50%;

  background: var(--accent-color);
  border: 1px solid rgba(0, 0, 0, 0.1);

  transition: background-color var(--transition-value),
    border-color var(--transition-value), fill var(--transition-value);
}

.modal-close:is(:hover, :focus) {
  background-color: var(--pressed-state-color);
  border-color: var(--pressed-state-color);
  fill: var(--hero-section-color);
}

.modal-title {
  margin-top: 16px;
  margin-bottom: 16px;
  font-size: 16px;
  font-weight: 500;
  line-height: calc(24 / 16);
  text-align: center;
  color: var(--heading-text-color);
}

@media screen and (min-width: 428px) {
  .modal {
    padding-top: 72px;
    min-width: 392px;
  }

  .modal-close {
    top: 24px;
    right: 24px;
  }

  .modal-title {
    margin-top: 0;
  }
}

.modal-input {
  width: 100%;
  border: 1px solid rgba(33, 33, 33, 0.2);
  border-radius: 4px;
  padding-left: 38px;
  padding-top: 8px;
  padding-bottom: 8px;

  margin-top: 4px;
  margin-bottom: 8px;

  outline: transparent;

  transition: border-color var(--transition-value);
}

.modal-label {
  font-size: 12px;
  line-height: 1.33;
  letter-spacing: 0.04em;
  color: var(--subtle-text-color);
}

.input-wrap {
  position: relative;
}

.modal-input-icon {
  position: absolute;
  left: 16px;
  top: 50%;
  transform: translateY(-50%);

  transition: fill var(--transition-value);
}

.modal-comment {
  width: 100%;
  height: 120px;
  outline: transparent;
  border: 1px solid rgba(33, 33, 33, 0.2);
  border-radius: 4px;
  padding-top: 8px;
  padding-left: 16px;

  margin-top: 4px;
  font-size: 12px;
  line-height: 1.33;
  letter-spacing: 0.04em;
  color: rgba(117, 117, 117, 0.5);
  resize: none;

  transition: border-color var(--transition-value);
}

.modal-input:focus,
.modal-comment:focus {
  border-color: var(--primary-color);
}

.modal-input:focus + .modal-input-icon {
  fill: var(--primary-color);
}

.check-text {
  margin-top: 16px;
  margin-bottom: 24px;

  font-size: 12px;
  line-height: 1.33;
  letter-spacing: 0.04em;
  color: #757575;

  display: flex;
}

.check-text span {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 16px;
  height: 16px;
  border: 1.25px solid var(--heading-text-color);
  border-radius: 2px;
  margin-right: 8px;
  fill: transparent;

  transition: background-color var(--transition-value),
    fill var(--transition-value), border var(--transition-value);
}

.modal-check:checked,
.modal-check:focus + .check-text span {
  background-color: var(--pressed-state-color);
  border-color: var(--pressed-state-color);
  fill: var(--hero-section-color);
}

.policy-link:visited {
  color: var(--primary-color);
}

.form-btn {
  display: block;
  margin-right: auto;
  margin-left: auto;
  width: 169px;

  padding-top: 16px;
  padding-right: 32px;
  padding-bottom: 16px;
  padding-left: 32px;
  border: 1px transparent;
  border-radius: 4px;

  font-weight: 500;
  line-height: 1.5;
  background-color: var(--primary-color);
  box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.15);
  color: var(--hero-section-color);
  letter-spacing: 0.04em;

  transition: background-color var(--transition-value);
}

.form-btn:hover,
.form-btn:focus {
  background-color: var(--pressed-state-color);
}
