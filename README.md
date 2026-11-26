
:root {
    --primary: #5278ad;
    --primary-dark: #3d6296;
    --primary-soft: #edf3fa;
    --background: #f4f6f8;
    --surface: #ffffff;
    --text: #303b49;
    --muted: #84909d;
    --border: #e5e9ee;
    --green: #438c70;
    --green-soft: #edf6f1;
    --red: #c96b6b;
    --red-soft: #fbefef;
    --orange: #b98b4d;
    --orange-soft: #faf4e9;
    --radius: 9px;
    --shadow: 0 1px 4px rgba(30, 45, 65, .035);
}

* {
    box-sizing: border-box;
}

body {
    margin: 0;
    background: var(--background);
    color: var(--text);
    font-family: Arial, Helvetica, sans-serif;
    font-size: 14px;
}

button, input, textarea, select {
    font: inherit;
}

button {
    cursor: pointer;
}

/* Боковое меню */

.sidebar {
    width: 235px;
    position: fixed;
    inset: 0 auto 0 0;
    background: var(--surface);
    border-right: 1px solid var(--border);
    padding: 20px 15px;
    z-index: 20;
    display: flex;
    flex-direction: column;
    transition: transform .2s;
}

.brand {
    display: flex;
    align-items: center;
    gap: 10px;
    padding: 0 8px 25px;
}

.brand-mark {
    width: 37px;
    height: 37px;
    border-radius: 8px;
    background: #eaf0f7;
    color: #456b9d;
    display: grid;
    place-items: center;
    font-size: 19px;
    font-weight: 700;
    border: 1px solid #dce5ef;
}

.brand-name {
    font-size: 16px;
    font-weight: 700;
    letter-spacing: .2px;
}

.brand-name span {
    color: var(--primary);
}

.brand-sub {
    color: var(--muted);
    font-size: 9px;
    margin-top: 3px;
    letter-spacing: .5px;
}

.menu-label {
    color: #9aa4af;
    font-size: 10px;
    font-weight: 700;
    letter-spacing: .7px;
    padding: 12px 11px 7px;
}

.nav {
    display: flex;
    flex-direction: column;
    gap: 3px;
}

.nav button {
    border: 0;
    background: transparent;
    color: #687585;
    padding: 10px 11px;
    text-align: left;
    border-radius: 6px;
    display: flex;
    align-items: center;
    gap: 11px;
    font-size: 13px;
    transition: background .15s;
}

.nav button:hover {
    background: #f3f5f8;
    color: var(--text);
}

.nav button.active {
    background: #edf2f8;
    color: #3e6598;
    font-weight: 600;
}

.nav-icon {
    width: 19px;
    text-align: center;
    font-size: 16px;
}

.sidebar-bottom {
    margin-top: auto;
    border-top: 1px solid var(--border);
    padding-top: 13px;
}

.user-mini {
    display: flex;
    align-items: center;
    gap: 10px;
    padding: 7px;
}

.avatar {
    width: 34px;
    height: 34px;
    background: #eaf0f7;
    color: #456b9d;
    border-radius: 50%;
    display: grid;
    place-items: center;
    font-weight: 700;
}

.user-mini small {
    display: block;
    color: var(--muted);
    margin-top: 4px;
    font-size: 11px;
}

/* Основная область */

.main {
    margin-left: 235px;
    min-height: 100vh;
}

.topbar {
    height: 62px;
    background: white;
    border-bottom: 1px solid var(--border);
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 0 29px;
    position: sticky;
    top: 0;
    z-index: 10;
}

.topbar-left {
    display: flex;
    align-items: center;
    gap: 12px;
}

.topbar h2 {
    font-size: 15px;
    font-weight: 600;
    margin: 0;
}

.topbar-right {
    display: flex;
    align-items: center;
    gap: 14px;
    color: var(--muted);
    font-size: 11px;
}

.online-dot {
    width: 7px;
    height: 7px;
    border-radius: 50%;
    background: #5a9c7c;
    display: inline-block;
    margin-right: 5px;
}

.menu-toggle {
    display: none;
    border: 0;
    background: transparent;
    font-size: 21px;
}

.content {
    max-width: 1450px;
    padding: 27px 29px;
    margin: auto;
}

.page {
    display: none;
}

.page.active {
    display: block;
}

.heading {
    display: flex;
    justify-content: space-between;
    align-items: center;
    gap: 15px;
    margin-bottom: 21px;
}

.heading h1 {
    margin: 0 0 6px;
    font-size: 22px;
    font-weight: 650;
}

.heading p {
    margin: 0;
    color: var(--muted);
    font-size: 12px;
}

/* Кнопки */

.btn {
    border: 1px solid #dfe4e9;
    border-radius: 6px;
    padding: 9px 13px;
    background: white;
    color: #596779;
    font-weight: 600;
    font-size: 12px;
    transition: .15s;
}

.btn:hover {
    background: #f5f7f9;
}

.btn-primary {
    color: white;
    background: #5278ad;
    border-color: #5278ad;
}

.btn-primary:hover {
    background: #3d6296;
}

.btn-danger {
    color: var(--red);
    background: white;
    border-color: #eadada;
}

.btn-success {
    color: var(--green);
    border-color: #d8e9df;
    background: var(--green-soft);
}

.btn-small {
    padding: 6px 9px;
    font-size: 11px;
}

.btn-row {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
}

/* Карточки */

.card {
    background: white;
    border: 1px solid var(--border);
    border-radius: 8px;
    padding: 18px;
    box-shadow: var(--shadow);
}

.stats-grid {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 13px;
    margin-bottom: 17px;
}

.stat-card {
    background: white;
    border: 1px solid var(--border);
    border-radius: 8px;
    padding: 16px;
    box-shadow: var(--shadow);
}

.stat-top {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 14px;
}

.stat-label {
    color: var(--muted);
    font-size: 11px;
}

.stat-icon {
    width: 31px;
    height: 31px;
    background: #eff3f8;
    color: #597ba6;
    border-radius: 7px;
    display: grid;
    place-items: center;
    font-size: 15px;
}

.stat-value {
    font-size: 25px;
    font-weight: 700;
}

.stat-description {
    font-size: 10px;
    color: var(--muted);
    margin-top: 6px;
}

.two-columns {
    display: grid;
    grid-template-columns: 1.4fr 1fr;
    gap: 14px;
    margin-bottom: 17px;
}

.card-title {
    display: flex;
    justify-content: space-between;
    align-items: center;
    gap: 10px;
    margin-bottom: 17px;
}

.card-title h3 {
    margin: 0;
    font-size: 14px;
    font-weight: 650;
}

.card-title span {
    color: var(--muted);
    font-size: 10px;
}

/* График */

.chart {
    height: 175px;
    display: flex;
    align-items: end;
    justify-content: space-around;
    gap: 14px;
    border-bottom: 1px solid var(--border);
    background: repeating-linear-gradient(
        to bottom,
        transparent 0,
        transparent 42px,
        #f0f2f5 43px
    );
    padding: 10px 5px 0;
}

.chart-column {
    height: 100%;
    flex: 1;
    display: flex;
    flex-direction: column;
    justify-content: end;
    align-items: center;
    gap: 7px;
}

.chart-bar {
    width: 60%;
    max-width: 34px;
    background: #91a9c8;
    border-radius: 4px 4px 0 0;
    min-height: 3px;
}

.chart-label {
    color: var(--muted);
    font-size: 10px;
    padding-bottom: 7px;
}

/* Активность */

.activity-list {
    display: flex;
    flex-direction: column;
    gap: 15px;
}

.activity {
    display: flex;
    align-items: center;
    gap: 10px;
}

.activity-symbol {
    width: 30px;
    height: 30px;
    border-radius: 7px;
    background: #eff3f8;
    color: #597ba6;
    display: grid;
    place-items: center;
}

.activity-text {
    flex: 1;
    font-size: 11px;
}

.activity-text small {
    display: block;
    color: var(--muted);
    margin-top: 4px;
}

.activity-time {
    font-size: 10px;
    color: var(--muted);
}

/* Таблицы */

.table-wrap {
    overflow-x: auto;
}

table {
    width: 100%;
    border-collapse: collapse;
    font-size: 12px;
}

th {
    text-align: left;
    padding: 12px 10px;
    color: #8994a1;
    font-size: 10px;
    border-bottom: 1px solid var(--border);
    white-space: nowrap;
}

td {
    padding: 13px 10px;
    border-bottom: 1px solid #eff1f4;
}

tr:last-child td {
    border-bottom: 0;
}

.status {
    padding: 4px 7px;
    border-radius: 4px;
    background: var(--green-soft);
    color: var(--green);
    font-size: 10px;
    display: inline-block;
}

.status.warning {
    color: var(--orange);
    background: var(--orange-soft);
}

.status.danger {
    color: var(--red);
    background: var(--red-soft);
}

.empty {
    padding: 27px 12px;
    text-align: center;
    color: var(--muted);
}

/* Формы */

.form-group {
    margin-bottom: 15px;
}

.form-group label {
    display: block;
    margin-bottom: 7px;
    font-size: 12px;
    font-weight: 600;
}

.field {
    width: 100%;
    border: 1px solid #dfe4e9;
    border-radius: 6px;
    padding: 10px 11px;
    color: var(--text);
    background: white;
    outline: none;
    font-size: 12px;
}

.field:focus {
    border-color: #7897bd;
}

textarea.field {
    min-height: 105px;
    resize: vertical;
}

.form-layout {
    max-width: 850px;
}

.info-box {
    padding: 12px 14px;
    border-radius: 6px;
    background: #f1f5fa;
    border: 1px solid #e3eaf2;
    color: #60758f;
    font-size: 11px;
    line-height: 1.65;
    margin-bottom: 16px;
}

.warning-box {
    padding: 12px 14px;
    background: var(--orange-soft);
    border: 1px solid #f0e5d2;
    color: #8c7045;
    border-radius: 6px;
    font-size: 11px;
    line-height: 1.6;
    margin-bottom: 16px;
}

.progress {
    height: 6px;
    border-radius: 10px;
    background: #edf0f4;
    overflow: hidden;
    margin-top: 8px;
}

.progress-fill {
    height: 100%;
    background: #7897bd;
    border-radius: 10px;
}

.question-card {
    padding: 15px;
    border: 1px solid var(--border);
    border-radius: 7px;
    margin-bottom: 12px;
    background: #fcfcfd;
}

.question-card h4 {
    margin: 0 0 12px;
    font-size: 12px;
}

.option {
    display: flex;
    align-items: center;
    gap: 8px;
    padding: 7px 0;
    font-size: 11px;
}

.option input {
    accent-color: var(--primary);
}

.search {
    max-width: 260px;
}

/* Симулятор */

.scenario {
    border: 1px solid var(--border);
    background: #fcfcfd;
    border-radius: 8px;
    padding: 17px;
    margin-bottom: 12px;
}

.scenario-header {
    display: flex;
    justify-content: space-between;
    gap: 10px;
    margin-bottom: 13px;
}

.scenario-message {
    background: white;
    border: 1px solid var(--border);
    border-radius: 6px;
    padding: 14px;
    line-height: 1.7;
    font-size: 12px;
    margin-bottom: 13px;
}

.choice-button {
    width: 100%;
    padding: 11px;
    text-align: left;
    border: 1px solid var(--border);
    background: white;
    border-radius: 6px;
    margin: 4px 0;
    color: var(--text);
    font-size: 11px;
}

.choice-button:hover {
    border-color: #91a9c8;
    background: #f5f8fb;
}

.answer-feedback {
    padding: 13px;
    margin-top: 12px;
    border-radius: 6px;
    font-size: 11px;
    line-height: 1.6;
}

/* Академия */

.learning-grid {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 13px;
}

.lesson-card {
    border: 1px solid var(--border);
    background: white;
    border-radius: 8px;
    padding: 17px;
}

.lesson-icon {
    width: 36px;
    height: 36px;
    border-radius: 7px;
    background: #eff3f8;
    color: #597ba6;
    display: grid;
    place-items: center;
    font-size: 17px;
    margin-bottom: 12px;
}

.lesson-card h3 {
    font-size: 13px;
    margin: 0 0 7px;
}

.lesson-card p {
    color: var(--muted);
    font-size: 11px;
    line-height: 1.65;
    min-height: 50px;
}

/* Достижения */

.achievement-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 12px;
}

.achievement {
    border: 1px solid var(--border);
    border-radius: 8px;
    padding: 16px;
    background: white;
}

.achievement.locked {
    opacity: .55;
    background: #fafbfc;
}

.achievement-icon {
    font-size: 23px;
    margin-bottom: 10px;
}

.achievement strong {
    display: block;
    font-size: 12px;
}

.achievement small {
    display: block;
    color: var(--muted);
    margin-top: 5px;
    font-size: 10px;
}

/* Модальное окно */

.modal {
    display: none;
    position: fixed;
    inset: 0;
    background: #26344966;
    z-index: 100;
    overflow: auto;
    padding: 22px;
}

.modal-content {
    background: white;
    border-radius: 9px;
    padding: 21px;
    max-width: 620px;
    margin: 35px auto;
    box-shadow: 0 8px 25px #2634491c;
}

.modal-header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 16px;
}

.modal-header h3 {
    margin: 0;
}

/* Адаптивность */

@media(max-width: 1100px) {
    .stats-grid {
        grid-template-columns: repeat(2, 1fr);
    }

    .two-columns {
        grid-template-columns: 1fr;
    }
}

@media(max-width: 720px) {
    .sidebar {
        transform: translateX(-100%);
    }

    .sidebar.open {
        transform: translateX(0);
    }

    .main {
        margin-left: 0;
    }

    .menu-toggle {
        display: block;
    }

    .content {
        padding: 20px 14px;
    }

    .topbar {
        padding: 0 14px;
    }

    .heading {
        align-items: flex-start;
        flex-direction: column;
    }

    .learning-grid {
        grid-template-columns: 1fr;
    }

    .achievement-grid {
        grid-template-columns: repeat(2, 1fr);
    }
}

@media(max-width: 430px) {
    .stats-grid {
        grid-template-columns: 1fr 1fr;
        gap: 8px;
    }

    .stat-card {
        padding: 12px;
    }

    .stat-value {
        font-size: 22px;
    }

    .achievement-grid {
        grid-template-columns: 1fr;
    }
}

@media print {
    .sidebar, .topbar, .no-print, .btn {
        display: none !important;
    }

    .main {
        margin: 0;
    }

    .content {
        padding: 0;
    }

    body {
        background: white;
    }

    .card {
        box-shadow: none;
    }
}
