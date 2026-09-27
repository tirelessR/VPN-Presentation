---
theme: default
transition: slide-left
mdc: true
fonts:
  sans: Ubuntu
  mono: Ubuntu Mono
  weights: 300,400,500,700
---

<div class="title-slide">

<div class="title-main">
  <h1>Технология VPN</h1>
  <h2>Архитектура, протоколы, безопасность</h2>
</div>

<div class="title-authors">
  <p>Выполнили студенты группы ИВТб-4302:</p>
  <p>Репин Иван Алексеевич</p>
  <p>Репина Марина Андреевна</p>
</div>

</div>

---
layout: default
---

<div class="vpn-definition-slide">

<div class="vpn-definition-left">

<h1>Что такое VPN?</h1>

<p class="vpn-definition-main">
<span class="vpn-definition-term">VPN</span> — технология создания
логического сетевого соединения
<span class="vpn-definition-accent">поверх другой сети</span>.
</p>

<p class="vpn-definition-secondary">
В качестве транспортной инфраструктуры может использоваться Интернет,
который рассматривается как потенциально недоверенная среда.
</p>

</div>

<div class="vpn-definition-right">

<span class="small-label">ФИЗИЧЕСКАЯ ИНФРАСТРУКТУРА</span>

<div class="vpn-simple-row">

<div class="simple-node">
  <strong>Сеть A</strong>
</div>

<div class="simple-connector"></div>

<div class="simple-node muted-node">
  <strong>Internet</strong>
</div>

<div class="simple-connector"></div>

<div class="simple-node">
  <strong>Сеть B</strong>
</div>

</div>

<div class="vpn-definition-separator"></div>

<span class="small-label">ЛОГИЧЕСКОЕ СОЕДИНЕНИЕ</span>

<div class="logical-channel">
  <div class="logical-end">A</div>
  <div class="logical-line"><span>VPN</span></div>
  <div class="logical-end">B</div>
</div>

</div>

<v-click>

<p class="vpn-definition-bottom">
Физически устройства могут находиться в разных сетях,
но VPN позволяет связать их <span>на логическом уровне</span>.
</p>

</v-click>

</div>

---
layout: default
---

<div class="vpn-security-slide">

<div class="slide-heading">

<h1>VPN и информационная безопасность</h1>

<p>
Защищённый VPN использует криптографические механизмы для передачи
данных через потенциально недоверенную сеть.
</p>

</div>

<div class="three-card-grid">

<div class="info-card">
<span class="card-number">01</span>
<h2>Конфиденциальность</h2>
<p>Передаваемая информация не должна быть доступна посторонним.</p>
<strong class="card-keyword">Шифрование</strong>
</div>

<div class="info-card">
<span class="card-number">02</span>
<h2>Целостность</h2>
<p>Несанкционированное изменение данных должно обнаруживаться.</p>
<strong class="card-keyword">Контроль изменений</strong>
</div>

<div class="info-card">
<span class="card-number">03</span>
<h2>Доступность</h2>
<p>Легитимный пользователь должен иметь доступ к системе, когда это необходимо.</p>
<strong class="card-keyword">Доступ к сервису</strong>
</div>

</div>

<v-click>

<div class="simple-note">
Стойкое шифрование само по себе не гарантирует безопасность всей VPN-инфраструктуры.
</div>

</v-click>

</div>

---
layout: default
---

<div class="standard-slide">

<div class="slide-heading">
<h1>Основные типы VPN</h1>
<p>Два наиболее распространённых сценария — подключение отдельного клиента и соединение целых сетей.</p>
</div>

<div class="two-card-grid">

<div class="large-card">

<h2>Remote Access VPN</h2>

<p class="card-intro">
Отдельный пользователь или устройство подключается к удалённой сети.
</p>

<div class="remote-scheme">
  <div class="scheme-node">Клиент</div>
  <div class="scheme-line"></div>
  <div class="scheme-node light-node">Internet</div>
  <div class="scheme-line"></div>
  <div class="scheme-node accent-node">VPN-шлюз</div>
</div>

<div class="scheme-result">
Корпоративная сеть
</div>

<p class="card-footer">
Удалённая работа, администрирование и доступ к внутренним ресурсам.
</p>

</div>

<div class="large-card">

<h2>Site-to-Site VPN</h2>

<p class="card-intro">
VPN-шлюзы соединяют две территориально удалённые локальные сети.
</p>

<div class="site-scheme">
  <div class="network-group">
    <span></span><span></span><span></span>
    <strong>Сеть A</strong>
  </div>

  <div class="site-tunnel">VPN</div>

  <div class="network-group">
    <span></span><span></span><span></span>
    <strong>Сеть B</strong>
  </div>
</div>

<p class="card-footer">
Конечным компьютерам не требуется самостоятельно устанавливать VPN-соединение.
</p>

</div>

</div>

</div>

---
layout: default
---

<div class="standard-slide">

<div class="slide-heading">
<h1>Основные компоненты VPN</h1>
<p>VPN-инфраструктура состоит не только из туннеля: каждая сторона выполняет собственную роль.</p>
</div>

<div class="component-grid">

<div class="component-card">

<div class="component-symbol">C</div>

<h2>VPN-клиент</h2>

<p>
Программное обеспечение или устройство, которое инициирует VPN-соединение.
</p>

<ul>
  <li>запускает подключение</li>
  <li>участвует в аутентификации</li>
  <li>передаёт трафик в VPN</li>
</ul>

</div>

<div class="component-card component-main">

<div class="component-symbol">T</div>

<h2>VPN-туннель</h2>

<p>
Логический канал, по которому инкапсулированный трафик передаётся через промежуточную сеть.
</p>

<ul>
  <li>инкапсуляция данных</li>
  <li>логическая связность</li>
  <li>передача между сторонами</li>
</ul>

</div>

<div class="component-card">

<div class="component-symbol">G</div>

<h2>VPN-шлюз</h2>

<p>
Сервер, маршрутизатор или межсетевой экран, обслуживающий VPN-соединения.
</p>

<ul>
  <li>обработка трафика</li>
  <li>маршрутизация</li>
  <li>политики безопасности</li>
</ul>

</div>

</div>

</div>

---
layout: default
---

<div class="standard-slide">

<div class="slide-heading">
<h1>Туннелирование</h1>
<p>При туннелировании исходные сетевые данные переносятся внутри другого сетевого представления.</p>
</div>

<div class="tunnel-demo">

<div class="packet-stage">

<span class="small-label">ИСХОДНЫЙ ПАКЕТ</span>

<div class="packet">
  <div class="packet-header">IP-заголовок</div>
  <div class="packet-data">Данные</div>
</div>

</div>

<div class="packet-transform">→</div>

<div class="packet-stage">

<span class="small-label">ПОСЛЕ ИНКАПСУЛЯЦИИ</span>

<div class="packet outer-packet">
  <div class="outer-header">Внешний заголовок</div>
  <div class="inner-packet">
    <span>IP-заголовок</span>
    <strong>Данные</strong>
  </div>
</div>

</div>

</div>

<div class="tunnel-difference">

<div>
<strong>Инкапсуляция</strong>
<p>Позволяет перенести данные одного протокола внутри другого.</p>
</div>

<div>
<strong>Шифрование</strong>
<p>Делает содержимое недоступным без соответствующего ключа.</p>
</div>

</div>

<v-click>

<div class="simple-note">
Туннелирование само по себе ещё не означает криптографическую защищённость.
</div>

</v-click>

</div>

---
layout: default
---

<div class="standard-slide">

<div class="slide-heading">
<h1>L2 и L3 VPN</h1>
<p>VPN-технологии можно различать по типу передаваемых данных и месту их работы в сетевой архитектуре.</p>
</div>

<div class="layer-grid">

<div class="layer-card">

<span class="layer-name">L2</span>

<h2>Канальный уровень</h2>

<p>
Работает с кадрами второго уровня и позволяет переносить канальную связность через другую инфраструктуру.
</p>

<div class="layer-example">
L2TP
</div>

</div>

<div class="layer-card">

<span class="layer-name accent-layer">L3</span>

<h2>Сетевой уровень</h2>

<p>
Работает прежде всего с IP-пакетами и естественно подходит для соединения IP-сетей.
</p>

<div class="layer-examples">
  <span>IPsec</span>
  <span>WireGuard</span>
</div>

</div>

</div>

<div class="layer-note">
Реальные VPN-системы могут комбинировать механизмы нескольких уровней.
</div>

</div>

---
layout: default
---

<div class="section-title-slide">

<span>VPN</span>
<h1>Основные протоколы</h1>

<p>
VPN — это не один протокол, а несколько технологий с разной архитектурой,
криптографией и областью применения.
</p>

</div>

---
layout: default
---

<div class="standard-slide">

<div class="slide-heading">
<h1>PPTP и L2TP/IPsec</h1>
<p>Два исторически распространённых подхода, которые сегодня занимают разное место в инфраструктуре.</p>
</div>

<div class="protocol-pair">

<div class="protocol-card old-protocol">

<h2>PPTP</h2>

<span class="protocol-full">Point-to-Point Tunneling Protocol</span>

<div class="protocol-status risk-status">
Устаревший
</div>

<p>
Был популярен благодаря простоте и широкой поддержке операционных систем.
</p>

<p>
Типичные схемы с MS-CHAPv2 и MPPE имеют серьёзные недостатки, поэтому PPTP не следует выбирать для новых защищённых систем.
</p>

</div>

<div class="protocol-card">

<h2>L2TP/IPsec</h2>

<span class="protocol-full">Layer Two Tunneling Protocol + IPsec</span>

<div class="protocol-stack">
  <span>L2TP</span>
  <small>туннелирование</small>
  <span>IPsec</span>
  <small>криптографическая защита</small>
</div>

<p>
Широко поддерживается существующими системами, но содержит дополнительный уровень обработки и инкапсуляции.
</p>

</div>

</div>

</div>

---
layout: default
---

<div class="standard-slide">

<div class="slide-heading">
<h1>OpenVPN</h1>
<p>Зрелое VPN-решение с открытым исходным кодом и гибкой моделью конфигурации.</p>
</div>

<div class="openvpn-layout">

<div class="openvpn-main">

<div class="protocol-feature-row">
<span>01</span>
<div>
<strong>TLS</strong>
<p>Используется для аутентификации и согласования параметров защищённого соединения.</p>
</div>
</div>

<div class="protocol-feature-row">
<span>02</span>
<div>
<strong>UDP или TCP</strong>
<p>В большинстве VPN-сценариев обычно предпочтителен UDP.</p>
</div>
</div>

<div class="protocol-feature-row">
<span>03</span>
<div>
<strong>Гибкость</strong>
<p>Большое количество настроек и широкая поддержка платформ.</p>
</div>
</div>

</div>

<div class="transport-compare">

<span class="small-label">ТРАНСПОРТ</span>

<div class="transport-block recommended-transport">
<strong>UDP</strong>
<p>Меньше дополнительной транспортной логики.</p>
</div>

<div class="transport-block">
<strong>TCP</strong>
<p>Полезен в отдельных сетях с ограничениями.</p>
</div>

</div>

</div>

<v-click>

<div class="simple-note">
TCP внутри TCP может приводить к дополнительным задержкам и неэффективным повторным передачам.
</div>

</v-click>

</div>

---
layout: default
---

<div class="standard-slide">

<div class="slide-heading">
<h1>WireGuard</h1>
<p>Современный минималистичный VPN-протокол с фиксированным набором криптографических механизмов.</p>
</div>

<div class="wireguard-layout">

<div class="crypto-set">

<div class="crypto-item">
<strong>ChaCha20</strong>
<span>шифрование</span>
</div>

<div class="crypto-item">
<strong>Poly1305</strong>
<span>аутентификация сообщений</span>
</div>

<div class="crypto-item">
<strong>Curve25519</strong>
<span>операции с ключами</span>
</div>

<div class="crypto-item">
<strong>BLAKE2s</strong>
<span>хеширование</span>
</div>

</div>

<div class="wireguard-peer">

<span class="small-label">МОДЕЛЬ ПИРОВ</span>

<div class="peer-row">
  <div class="peer-box">Peer A</div>
  <div class="peer-channel">UDP</div>
  <div class="peer-box">Peer B</div>
</div>

<div class="peer-properties">
<p>Идентификация по открытым ключам</p>
<p>AllowedIPs определяет допустимые IP-префиксы</p>
</div>

</div>

</div>

<v-click>

<div class="simple-note">
Минимализм уменьшает число криптографических вариантов, но производительность всё равно зависит от системы и сети.
</div>

</v-click>

</div>

---
layout: default
---

<div class="standard-slide">

<div class="slide-heading">
<h1>IKEv2/IPsec</h1>
<p>Стандартизированный подход к защите IP-трафика и управлению параметрами защищённого соединения.</p>
</div>

<div class="ike-layout">

<div class="ike-card">
<span>01</span>
<h2>Аутентификация</h2>
<p>Стороны подтверждают свою подлинность.</p>
</div>

<div class="ike-card">
<span>02</span>
<h2>Согласование</h2>
<p>IKEv2 определяет параметры защиты и ключевой материал.</p>
</div>

<div class="ike-card">
<span>03</span>
<h2>IPsec</h2>
<p>Обеспечивает защищённую передачу IP-трафика.</p>
</div>

</div>

<div class="mobike-block">

<div>
<strong>MOBIKE</strong>
<p>Позволяет адаптировать соединение при изменении сетевого адреса клиента.</p>
</div>

<div class="mobike-example">
  <span>Wi-Fi</span>
  <b>→</b>
  <span>4G / 5G</span>
</div>

</div>

</div>

---
layout: default
---

<div class="standard-slide">

<div class="slide-heading">
<h1>Сравнение VPN-технологий</h1>
<p>Выбор определяется требованиями инфраструктуры, а не существованием одного «лучшего» протокола.</p>
</div>

<div class="protocol-table">

<div class="protocol-table-head">
  <span>Технология</span>
  <span>Характеристика</span>
  <span>Применение</span>
</div>

<div class="protocol-table-row faded-row">
  <strong>PPTP</strong>
  <span>устаревший</span>
  <span>историческая инфраструктура</span>
</div>

<div class="protocol-table-row">
  <strong>L2TP/IPsec</strong>
  <span>широкая совместимость</span>
  <span>существующие системы</span>
</div>

<div class="protocol-table-row">
  <strong>OpenVPN</strong>
  <span>гибкий и зрелый</span>
  <span>универсальный удалённый доступ</span>
</div>

<div class="protocol-table-row">
  <strong>WireGuard</strong>
  <span>компактный и современный</span>
  <span>современные VPN-сценарии</span>
</div>

<div class="protocol-table-row">
  <strong>IKEv2/IPsec</strong>
  <span>стандартизированный</span>
  <span>мобильный и корпоративный доступ</span>
</div>

</div>

</div>

---
layout: default
---

<div class="section-title-slide">

<span>VPN</span>
<h1>Криптографические основы</h1>

<p>
VPN должен не только передать пакет, но и обеспечить конфиденциальность,
целостность, аутентичность и безопасное управление ключами.
</p>

</div>

---
layout: default
---

<div class="standard-slide">

<div class="slide-heading">
<h1>Шифрование</h1>
<p>Для защиты большого объёма сетевого трафика применяются симметричные криптографические алгоритмы.</p>
</div>

<div class="encryption-grid">

<div class="encryption-card">

<h2>AES</h2>

<div class="key-lengths">
  <span>128</span>
  <span>192</span>
  <span>256</span>
</div>

<p>
Стандартизированный блочный шифр. В VPN часто используется в составе современных режимов защиты.
</p>

</div>

<div class="encryption-card">

<h2>ChaCha20</h2>

<div class="cipher-line">
  <span>ChaCha20</span>
  <b>+</b>
  <span>Poly1305</span>
</div>

<p>
Потоковый шифр, широко применяемый совместно с Poly1305 для аутентификации сообщений.
</p>

</div>

</div>

<div class="aead-block">

<strong>AEAD</strong>

<p>
Authenticated Encryption with Associated Data одновременно обеспечивает
конфиденциальность и проверку аутентичности данных.
</p>

<span>AES-GCM</span>
<span>ChaCha20-Poly1305</span>

</div>

</div>

---
layout: default
---

<div class="standard-slide">

<div class="slide-heading">
<h1>Аутентификация</h1>
<p>Перед предоставлением доступа VPN-система должна определить, кто именно устанавливает соединение.</p>
</div>

<div class="auth-grid">

<div class="auth-method">Пароль</div>
<div class="auth-method">Сертификат</div>
<div class="auth-method">PSK</div>
<div class="auth-method">Открытый ключ</div>
<div class="auth-method">Аппаратный токен</div>
<div class="auth-method">Одноразовый код</div>

</div>

<v-click>

<div class="mfa-block">

<div class="mfa-title">
<strong>MFA</strong>
<span>Multi-Factor Authentication</span>
</div>

<div class="mfa-factors">
  <span>пароль</span>
  <b>+</b>
  <span>второй фактор</span>
  <b>=</b>
  <strong>усиленная аутентификация</strong>
</div>

</div>

</v-click>

</div>

---
layout: default
---

<div class="standard-slide">

<div class="slide-heading">
<h1>Согласование ключей</h1>
<p>Сторонам необходимо получить общий секрет, не передавая этот секрет напрямую через недоверенную сеть.</p>
</div>

<div class="dh-layout">

<div class="dh-side">
<span>A</span>
<strong>Сторона A</strong>
<small>собственный секрет</small>
</div>

<div class="dh-middle">

<div class="dh-public">
Публичные параметры
</div>

<div class="dh-shared">
<strong>Общий секрет</strong>
<span>не передаётся по сети напрямую</span>
</div>

</div>

<div class="dh-side">
<span>B</span>
<strong>Сторона B</strong>
<small>собственный секрет</small>
</div>

</div>

<div class="dh-note-grid">

<div>
<strong>Diffie–Hellman</strong>
<p>Позволяет согласовать общий секрет через открытый канал.</p>
</div>

<div>
<strong>Аутентификация необходима</strong>
<p>Без проверки стороны остаётся риск Man-in-the-Middle.</p>
</div>

</div>

</div>

---
layout: default
---

<div class="standard-slide">

<div class="slide-heading">
<h1>Forward Secrecy</h1>
<p>Компрометация долгосрочного ключа не должна автоматически раскрывать ранее завершённые защищённые сеансы.</p>
</div>

<div class="forward-layout">

<div class="forward-timeline">

<div class="session-item">
<span>Сеанс 01</span>
<strong>ключ K₁</strong>
</div>

<div class="session-item">
<span>Сеанс 02</span>
<strong>ключ K₂</strong>
</div>

<div class="session-item">
<span>Сеанс 03</span>
<strong>ключ K₃</strong>
</div>

</div>

<div class="compromise-block">

<span>позже</span>

<div class="long-key">
<strong>Долгосрочный ключ</strong>
<small>скомпрометирован</small>
</div>

</div>

</div>

<v-click>

<div class="simple-note">
Эфемерный ключевой материал ограничивает последствия поздней компрометации долгосрочного секрета.
</div>

</v-click>

</div>

---
layout: default
---

<div class="section-title-slide">

<span>VPN</span>
<h1>Угрозы и безопасность</h1>

<p>
Безопасность VPN зависит не только от криптографии,
но и от аутентификации, маршрутизации, DNS, конфигурации и конечных устройств.
</p>

</div>

---
layout: default
---

<div class="standard-slide">

<div class="slide-heading">
<h1>Man-in-the-Middle</h1>
<p>Злоумышленник пытается оказаться между сторонами соединения и выдать себя за одну из них.</p>
</div>

<div class="mitm-layout">

<div class="mitm-node">
<strong>Клиент</strong>
<span>ожидает VPN-шлюз</span>
</div>

<div class="mitm-connection">
  <span>соединение</span>
</div>

<div class="mitm-attacker">
<strong>Злоумышленник</strong>
<span>пытается подменить сторону</span>
</div>

<div class="mitm-connection">
  <span>соединение</span>
</div>

<div class="mitm-node">
<strong>VPN-шлюз</strong>
<span>ожидает клиента</span>
</div>

</div>

<div class="mitm-protection">

<div>
<span>01</span>
<strong>Аутентификация</strong>
</div>

<div>
<span>02</span>
<strong>Проверка сертификатов / ключей</strong>
</div>

<div>
<span>03</span>
<strong>Защищённое согласование ключей</strong>
</div>

</div>

</div>

---
layout: default
---

<div class="standard-slide">

<div class="slide-heading">
<h1>Утечки трафика</h1>
<p>Даже активный VPN не гарантирует, что абсолютно весь трафик автоматически проходит по ожидаемому маршруту.</p>
</div>

<div class="leak-grid">

<div class="leak-card">

<h2>DNS leak</h2>

<div class="leak-path">
  <span>VPN-трафик</span>
  <strong>VPN</strong>
</div>

<div class="leak-path bad-path">
  <span>DNS-запрос</span>
  <strong>локальная сеть</strong>
</div>

<p>
DNS-запросы могут уходить вне предусмотренного VPN-маршрута и раскрывать запрашиваемые домены.
</p>

</div>

<div class="leak-card">

<h2>IP leak</h2>

<div class="ip-stack">
  <span>IPv4 → VPN</span>
  <span class="bad-ip">IPv6 → другой маршрут</span>
</div>

<p>
Неправильная маршрутизация или неполная поддержка IPv6 способны привести к обходу туннеля частью трафика.
</p>

</div>

</div>

</div>

---
layout: default
---

<div class="standard-slide">

<div class="slide-heading">
<h1>Full Tunnel и Split Tunneling</h1>
<p>Политика маршрутизации определяет, какой трафик клиента необходимо передавать через VPN.</p>
</div>

<div class="tunnel-mode-grid">

<div class="tunnel-mode-card">

<h2>Full Tunnel</h2>

<div class="traffic-list full-traffic">
  <span>Корпоративные ресурсы</span>
  <span>Web</span>
  <span>DNS</span>
  <span>Другой трафик</span>
</div>

<strong class="mode-result">всё через VPN</strong>

<p>
Централизованный контроль, но большая нагрузка на VPN-инфраструктуру.
</p>

</div>

<div class="tunnel-mode-card">

<h2>Split Tunneling</h2>

<div class="traffic-list">
  <span class="vpn-traffic">Корпоративные ресурсы</span>
  <span>Web напрямую</span>
  <span>Другой трафик напрямую</span>
</div>

<strong class="mode-result">VPN только для выбранных сетей</strong>

<p>
Меньше нагрузки, но политика маршрутизации и безопасности становится сложнее.
</p>

</div>

</div>

</div>

---
layout: default
---

<div class="standard-slide">

<div class="slide-heading">
<h1>Downgrade-атаки</h1>
<p>Атакующий пытается заставить систему использовать более слабую версию протокола или криптографических параметров.</p>
</div>

<div class="downgrade-layout">

<div class="versions">

<div class="version-block current-version">
  <span>современный</span>
  <strong>Protocol v3</strong>
</div>

<div class="version-block">
  <span>старый</span>
  <strong>Protocol v2</strong>
</div>

<div class="version-block weak-version">
  <span>устаревший</span>
  <strong>Protocol v1</strong>
</div>

</div>

<div class="downgrade-action">

<strong>Цель атаки</strong>
<p>Перевести взаимодействие на более слабый поддерживаемый вариант.</p>

<div class="downgrade-protection">
Отключать устаревшие версии и алгоритмы, если они больше не нужны.
</div>

</div>

</div>

</div>

---
layout: default
---

<div class="standard-slide">

<div class="slide-heading">
<h1>Практические меры защиты</h1>
<p>Безопасная эксплуатация VPN требует защиты всей инфраструктуры, а не только выбора криптографического алгоритма.</p>
</div>

<div class="security-measures">

<div>
<span>01</span>
<strong>Современные протоколы</strong>
<p>Отключать устаревшие технологии и слабые параметры.</p>
</div>

<div>
<span>02</span>
<strong>MFA</strong>
<p>Использовать многофакторную аутентификацию для удалённого доступа.</p>
</div>

<div>
<span>03</span>
<strong>Обновления</strong>
<p>Своевременно обновлять VPN-шлюзы и клиенты.</p>
</div>

<div>
<span>04</span>
<strong>Маршрутизация</strong>
<p>Контролировать IPv4, IPv6, DNS и правила туннелирования.</p>
</div>

<div>
<span>05</span>
<strong>Мониторинг</strong>
<p>Вести журналирование и отслеживать подозрительные события.</p>
</div>

<div>
<span>06</span>
<strong>Минимальные привилегии</strong>
<p>Не предоставлять больше доступа, чем действительно требуется.</p>
</div>

</div>

</div>

---
layout: default
---

<div class="section-title-slide">

<span>VPN</span>
<h1>Современное развитие</h1>

<p>
Современная инфраструктура уходит от идеи автоматического доверия
на основании одного лишь сетевого местоположения.
</p>

</div>

---
layout: default
---

<div class="standard-slide">

<div class="slide-heading">
<h1>Zero Trust</h1>
<p>Нахождение пользователя внутри корпоративной сети само по себе не является достаточным основанием для доверия.</p>
</div>

<div class="zero-layout">

<div class="zero-main">
<strong>Never trust implicitly</strong>
<span>Проверять запрос с учётом контекста</span>
</div>

<div class="zero-context">

<div>
<span>01</span>
<strong>Пользователь</strong>
</div>

<div>
<span>02</span>
<strong>Устройство</strong>
</div>

<div>
<span>03</span>
<strong>Ресурс</strong>
</div>

<div>
<span>04</span>
<strong>Контекст</strong>
</div>

<div>
<span>05</span>
<strong>Политика</strong>
</div>

</div>

</div>

<v-click>

<div class="simple-note">
Zero Trust — это архитектурный подход, а не отдельный VPN-протокол или продукт.
</div>

</v-click>

</div>

---
layout: default
---

<div class="standard-slide">

<div class="slide-heading">
<h1>VPN и ZTNA</h1>
<p>ZTNA развивает принцип Zero Trust применительно к доступу пользователей к приложениям и ресурсам.</p>
</div>

<div class="ztna-grid">

<div class="ztna-card">

<h2>Remote Access VPN</h2>

<div class="access-visual">
  <div class="access-user">User</div>
  <div class="access-network">Сеть / сегмент</div>
</div>

<p>
Обычно предоставляет определённую сетевую связность, которая затем ограничивается маршрутами и политиками.
</p>

</div>

<div class="ztna-card ztna-accent">

<h2>ZTNA</h2>

<div class="access-visual">
  <div class="access-user">User</div>
  <div class="access-network">Конкретный ресурс</div>
</div>

<p>
Стремится предоставлять доступ к определённому приложению после проверки идентичности, устройства и политики.
</p>

</div>

</div>

<div class="ztna-note">
ZTNA не обязано полностью заменять VPN — обе технологии могут использоваться одновременно.
</div>

</div>

---
layout: default
---

<div class="standard-slide">

<div class="slide-heading">
<h1>SD-WAN</h1>
<p>Software-Defined WAN позволяет централизованно управлять каналами связи распределённой организации.</p>
</div>

<div class="sdwan-layout">

<div class="branch-office">
<strong>Филиал</strong>
<span>локальная сеть</span>
</div>

<div class="wan-channels">

<div>
<span>Internet</span>
<small>основной канал</small>
</div>

<div>
<span>MPLS</span>
<small>корпоративная сеть</small>
</div>

<div>
<span>4G / 5G</span>
<small>резервный канал</small>
</div>

</div>

<div class="sdwan-controller">

<strong>SD-WAN</strong>

<p>
Выбор пути по политике, задержке, потерям и типу приложения.
</p>

</div>

</div>

<div class="simple-note always-visible-note">
Защищённые туннели являются частью многих SD-WAN-решений, но SD-WAN решает более широкую задачу управления WAN.
</div>

</div>

---
layout: default
---

<div class="standard-slide">

<div class="slide-heading">
<h1>SASE</h1>
<p>Secure Access Service Edge объединяет сетевые и защитные функции в общей архитектуре предоставления сервисов.</p>
</div>

<div class="sase-layout">

<div class="sase-center">
<strong>SASE</strong>
<span>Network + Security</span>
</div>

<div class="sase-grid">
  <div>SD-WAN</div>
  <div>ZTNA</div>
  <div>Secure Web Gateway</div>
  <div>CASB</div>
  <div>Firewall-as-a-Service</div>
  <div>Политики доступа</div>
</div>

</div>

<div class="sase-bottom">
Политики применяются ближе к пользователям, устройствам и приложениям — не обязательно через один центральный VPN-шлюз.
</div>

</div>

---
layout: default
---

<div class="standard-slide">

<div class="slide-heading">
<h1>Как меняется модель доступа?</h1>
<p>Новые подходы не обязательно заменяют старые: меняются архитектура доступа и модель доверия.</p>
</div>

<div class="evolution-list">

<div class="evolution-row">
<span>01</span>
<strong>Сетевой периметр</strong>
<p>Основное различие — внутри или снаружи корпоративной сети.</p>
</div>

<div class="evolution-row">
<span>02</span>
<strong>Remote Access VPN</strong>
<p>Защищённое подключение удалённого пользователя к инфраструктуре.</p>
</div>

<div class="evolution-row">
<span>03</span>
<strong>Zero Trust / ZTNA</strong>
<p>Доступ зависит от идентичности, устройства, ресурса и контекста.</p>
</div>

<div class="evolution-row">
<span>04</span>
<strong>SD-WAN / SASE</strong>
<p>Сетевые и защитные функции управляются как единая распределённая архитектура.</p>
</div>

</div>

</div>

---
layout: default
---

<div class="standard-slide conclusion-slide">

<h1>Заключение</h1>

<div class="conclusion-list">

<div>
<span>01</span>
<strong>VPN создаёт логическое соединение поверх другой сети</strong>
</div>

<div>
<span>02</span>
<strong>Безопасность зависит не только от шифрования, но и от всей архитектуры</strong>
</div>

<div>
<span>03</span>
<strong>Не существует одного универсально лучшего VPN-протокола</strong>
</div>

<div>
<span>04</span>
<strong>Zero Trust и ZTNA дополняют современную модель защищённого доступа</strong>
</div>

</div>

<v-click>

<div class="final-thanks">
Спасибо за внимание!
</div>

</v-click>

</div>