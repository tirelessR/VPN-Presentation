---
theme: default
transition: slide-left
mdc: true
fonts:
  sans: Ubuntu
  weights: 400
---

<style src="./styles/index.css"></style>
<div class="title-slide">
  <div class="title-content">
    <h1>Технология VPN</h1>
    <p class="title-subtitle">Принцип работы, применение и безопасность</p>
  </div>
  <div class="title-authors">
    <strong>Выполнили студенты группы ИВТб-4302:</strong>
    <strong>Репин Иван Алексеевич</strong>
    <strong>Репина Марина Андреевна</strong>
  </div>
</div>

---

<div class="intro-slide">
  <div class="slide-heading">
    <span>01</span>
    <span>ВВЕДЕНИЕ</span>
  </div>
  <h1>Что такое VPN?</h1>
  <div class="intro-main">
    <div class="definition-block">
      <p><strong>Virtual Private Network</strong> — технология, которая создаёт защищённое соединение между устройством пользователя и удалённым сервером или сетью.</p>
    </div>
    <div class="vpn-visual">
      <div class="device">
        <div class="computer-icon">
          <div class="computer-screen"></div>
          <div class="computer-stand"></div>
        </div>
        <span>Устройство</span>
      </div>
      <div class="vpn-connection">
        <div class="vpn-cable">
          <div class="vpn-data"></div>
        </div>
        <span>VPN-туннель</span>
      </div>
      <div class="device">
        <div class="server-icon">
          <div class="server-unit"><i></i><i></i></div>
          <div class="server-unit"><i></i><i></i></div>
          <div class="server-unit"><i></i><i></i></div>
        </div>
        <span>VPN-сервер</span>
      </div>
    </div>
  </div>
  <div class="vpn-features">
    <div class="vpn-feature">
      <span class="feature-number">01</span>
      <h3>Защищённый канал</h3>
      <p>Трафик проходит через VPN-туннель.</p>
    </div>
    <div class="vpn-feature">
      <span class="feature-number">02</span>
      <h3>Шифрование</h3>
      <p>Данные передаются в зашифрованном виде.</p>
    </div>
    <div class="vpn-feature">
      <span class="feature-number">03</span>
      <h3>Удалённый доступ</h3>
      <p>Безопасное подключение к ресурсам другой сети.</p>
    </div>
  </div>
</div>

---

<div class="history-slide">
  <div class="slide-heading">
    <span>02</span>
    <span>ИСТОРИЯ</span>
  </div>
  <h1>Как развивался VPN</h1>
  <div class="history-stages">
    <div v-click class="history-stage">
      <div class="history-year">1990-е</div>
      <h3>PPTP</h3>
      <p>Один из первых широко известных VPN-протоколов, разработанный при участии Microsoft.</p>
    </div>
    <div v-click class="history-stage">
      <div class="history-year">1990-е</div>
      <h3>IPsec</h3>
      <p>Появляются более надёжные механизмы защиты сетевого трафика.</p>
    </div>
    <div v-click class="history-stage">
      <div class="history-year">2001</div>
      <h3>OpenVPN</h3>
      <p>Открытое и гибкое решение, которое получило широкое распространение.</p>
    </div>
    <div v-click class="history-stage history-stage-current">
      <div class="history-year">2010-е</div>
      <h3>WireGuard</h3>
      <p>Современный протокол, ориентированный на безопасность, простоту и производительность.</p>
    </div>
  </div>
  <p v-click class="history-result">Со временем VPN вышел за пределы корпоративных сетей и стал массовой пользовательской технологией.</p>
</div>

---

<div class="connection-slide">
  <div class="slide-heading">
    <span>03</span>
    <span>ПРИНЦИП РАБОТЫ</span>
  </div>
  <h1>Обычное интернет-соединение</h1>
  <div class="connection-flow">
    <div class="connection-point">
      <div class="connection-computer">
        <div class="connection-screen"></div>
        <div class="connection-stand"></div>
      </div>
      <h3>Устройство</h3>
      <p>Отправляет запрос</p>
    </div>
    <div class="connection-arrow"><span>→</span></div>
    <div class="connection-point">
      <div class="provider-icon"><span>ISP</span></div>
      <h3>Провайдер</h3>
      <p>Передаёт трафик</p>
    </div>
    <div class="connection-arrow"><span>→</span></div>
    <div class="connection-point">
      <div class="website-icon">
        <div class="website-top"><i></i><i></i><i></i></div>
        <div class="website-content">www</div>
      </div>
      <h3>Сайт</h3>
      <p>Получает запрос</p>
    </div>
  </div>
  <div class="connection-notes">
    <p><strong>IP-адрес</strong> позволяет определить, откуда пришёл запрос и куда необходимо отправить ответ.</p>
    <p><strong>HTTPS</strong> шифрует содержимое соединения между браузером и сайтом, но не является VPN.</p>
  </div>
</div>

---

<div class="vpn-work-slide">
  <div class="slide-heading">
    <span>04</span>
    <span>ПРИНЦИП РАБОТЫ</span>
  </div>
  <h1>Как работает VPN</h1>
  <div class="vpn-work-flow">
    <div class="vpn-work-point">
      <div class="work-computer">
        <div class="work-screen"></div>
        <div class="work-stand"></div>
      </div>
      <h3>Устройство</h3>
      <p>Исходный IP-адрес</p>
    </div>
    <div class="tunnel-block">
      <div class="tunnel-label">ЗАШИФРОВАНО</div>
      <div class="tunnel-cable"><span>VPN</span></div>
      <p>Защищённый туннель</p>
    </div>
    <div class="vpn-work-point">
      <div class="work-server">
        <div><i></i><i></i></div>
        <div><i></i><i></i></div>
        <div><i></i><i></i></div>
      </div>
      <h3>VPN-сервер</h3>
      <p>Промежуточная точка</p>
    </div>
    <div class="internet-connection">
      <span>→</span>
      <p>Интернет</p>
    </div>
    <div class="vpn-work-point">
      <div class="work-website">
        <div class="work-website-top"><i></i><i></i><i></i></div>
        <div class="work-website-content">www</div>
      </div>
      <h3>Сайт</h3>
      <p>Видит IP VPN-сервера</p>
    </div>
  </div>
</div>

---

<div class="types-slide">
  <div class="slide-heading">
    <span>05</span>
    <span>ВИДЫ VPN</span>
  </div>
  <h1>Основные виды VPN</h1>
  <div class="vpn-types">
    <div class="vpn-type">
      <div class="type-diagram">
        <div class="mini-laptop">
          <div class="mini-laptop-screen"></div>
          <div class="mini-laptop-base"></div>
        </div>
        <div class="mini-tunnel"><span>VPN</span></div>
        <div class="mini-office">
          <div class="office-title">Сеть</div>
          <div class="office-pcs"><i></i><i></i><i></i></div>
        </div>
      </div>
      <h3>Remote Access</h3>
      <p>Один пользователь подключается к удалённой корпоративной сети.</p>
      <span class="type-example">Сотрудник из дома → сеть компании</span>
    </div>
    <div class="vpn-type">
      <div class="type-diagram">
        <div class="mini-office">
          <div class="office-title">Офис A</div>
          <div class="office-pcs"><i></i><i></i><i></i></div>
        </div>
        <div class="mini-tunnel"><span>VPN</span></div>
        <div class="mini-office">
          <div class="office-title">Офис B</div>
          <div class="office-pcs"><i></i><i></i><i></i></div>
        </div>
      </div>
      <h3>Site-to-Site</h3>
      <p>Защищённый туннель объединяет две удалённые локальные сети.</p>
      <span class="type-example">Сеть офиса A → сеть офиса B</span>
    </div>
    <div class="vpn-type vpn-type-accent">
      <div class="type-diagram commercial-diagram">
        <div class="mini-laptop">
          <div class="mini-laptop-screen"></div>
          <div class="mini-laptop-base"></div>
        </div>
        <div class="mini-tunnel"><span>VPN</span></div>
        <div class="mini-server"><i></i><i></i><i></i></div>
        <div class="mini-internet-arrow">→</div>
        <div class="mini-globe">WWW</div>
      </div>
      <h3>Коммерческий VPN</h3>
      <p>Трафик пользователя сначала проходит через сервер VPN-провайдера.</p>
      <span class="type-example">Устройство → VPN-сервер → интернет</span>
    </div>
  </div>
</div>

---

<div class="protocols-slide">
  <div class="slide-heading">
    <span>06</span>
    <span>VPN-ПРОТОКОЛЫ</span>
  </div>
  <h1>VPN-протоколы</h1>
  <div class="protocol-list">
    <div class="protocol-row protocol-modern">
      <div class="protocol-name">
        <h3>WireGuard</h3>
        <span>Современный</span>
      </div>
      <p>Компактный протокол, ориентированный на высокую скорость, безопасность и простоту реализации.</p>
      <div class="protocol-use">
        <span>Высокая скорость</span>
        <span>Простой код</span>
      </div>
    </div>
    <div class="protocol-row">
      <div class="protocol-name">
        <h3>OpenVPN</h3>
        <span>с 2001 года</span>
      </div>
      <p>Проверенное открытое решение с широкой поддержкой операционных систем и гибкой настройкой.</p>
      <div class="protocol-use">
        <span>Гибкость</span>
        <span>Совместимость</span>
      </div>
    </div>
    <div class="protocol-row">
      <div class="protocol-name">
        <h3>IPsec / IKEv2</h3>
        <span>Распространённый</span>
      </div>
      <p>Часто применяется в корпоративных сетях и на смартфонах, хорошо восстанавливает соединение после смены сети.</p>
      <div class="protocol-use">
        <span>Корпоративные сети</span>
        <span>Мобильные устройства</span>
      </div>
    </div>
    <div class="protocol-row protocol-old">
      <div class="protocol-name">
        <h3>PPTP</h3>
        <span>Устаревший</span>
      </div>
      <p>Один из ранних VPN-протоколов. Сегодня считается небезопасным и не рекомендуется к использованию.</p>
      <div class="protocol-use">
        <span>Слабая защита</span>
        <span>Не рекомендуется</span>
      </div>
    </div>
  </div>
</div>

---

<div class="uses-slide">
  <div class="slide-heading">
    <span>07</span>
    <span>ПРИМЕНЕНИЕ</span>
  </div>
  <h1>Для чего используется VPN</h1>
  <div class="uses-layout">
    <div class="use-item use-remote">
      <div class="use-number">01</div>
      <div>
        <h3>Удалённая работа</h3>
        <p>Доступ к внутренним файлам и сервисам компании из дома или командировки.</p>
      </div>
    </div>
    <div class="use-item use-wifi">
      <div class="use-number">02</div>
      <div>
        <h3>Общественный Wi-Fi</h3>
        <p>Шифрование соединения до VPN-сервера в гостиницах, аэропортах и кафе.</p>
      </div>
    </div>
    <div class="uses-center">
      <div class="central-server">
        <div class="central-server-unit"><i></i><i></i></div>
        <div class="central-server-unit"><i></i><i></i></div>
        <div class="central-server-unit"><i></i><i></i></div>
      </div>
      <h3>VPN</h3>
      <p>Защищённое соединение</p>
    </div>
    <div class="use-item use-location">
      <div class="use-number">03</div>
      <div>
        <h3>Точка выхода</h3>
        <p>Сайты видят IP-адрес выбранного VPN-сервера, который может находиться в другом регионе.</p>
      </div>
    </div>
    <div class="use-item use-offices">
      <div class="use-number">04</div>
      <div>
        <h3>Связь между офисами</h3>
        <p>Объединение удалённых корпоративных сетей через защищённое соединение.</p>
      </div>
    </div>
  </div>
</div>

---

<div class="advantages-slide">
  <div class="slide-heading">
    <span>08</span>
    <span>ПРЕИМУЩЕСТВА</span>
  </div>
  <h1>Что даёт использование VPN?</h1>
  <div class="advantages-grid">
    <div class="advantage-block">
      <div class="advantage-visual encryption-visual">
        <div class="data-open">DATA</div>
        <div class="data-arrow">→</div>
        <div class="data-encrypted">••••••</div>
      </div>
      <div class="advantage-content">
        <span class="advantage-number">01</span>
        <h3>Защита данных в пути</h3>
        <p>Трафик между устройством и VPN-сервером передаётся внутри зашифрованного туннеля.</p>
      </div>
    </div>
    <div class="advantage-block">
      <div class="advantage-visual ip-visual">
        <div class="ip-address ip-original">95.24.•••.••</div>
        <div class="ip-change">→</div>
        <div class="ip-address ip-vpn">VPN IP</div>
      </div>
      <div class="advantage-content">
        <span class="advantage-number">02</span>
        <h3>Сокрытие исходного IP</h3>
        <p>Для сайтов точкой выхода становится VPN-сервер, поэтому исходный публичный IP обычно им не виден.</p>
      </div>
    </div>
    <div class="advantage-block">
      <div class="advantage-visual access-visual">
        <div class="access-user"></div>
        <div class="access-tunnel">VPN</div>
        <div class="access-network">
          <i></i><i></i><i></i>
        </div>
      </div>
      <div class="advantage-content">
        <span class="advantage-number">03</span>
        <h3>Доступ к закрытым сетям</h3>
        <p>Пользователь может защищённо обращаться к ресурсам, которые не должны быть напрямую доступны из интернета.</p>
      </div>
    </div>
  </div>
</div>

---
<div class="limits-visual-slide">
  <div class="slide-heading">
    <span>09</span>
    <span>ОГРАНИЧЕНИЯ</span>
  </div>
  <h1>Что VPN не может?</h1>
  <div class="limits-main">
    <div class="limits-items">
      <div class="limit-item">
        <div class="limit-speed">
          <span>100</span>
          <b>→</b>
          <span>72</span>
        </div>
        <h3>Гарантировать скорость</h3>
        <p>Дополнительный сервер может увеличить задержку и снизить скорость соединения.</p>
      </div>
      <div class="limit-item">
        <div class="limit-identity">
          <span>IP</span>
          <b>≠</b>
          <div class="limit-person">
            <i></i>
            <i></i>
          </div>
        </div>
        <h3>Обеспечить анонимность</h3>
        <p>Аккаунты, cookie и другие идентификаторы продолжают работать после смены IP.</p>
      </div>
      <div class="limit-item">
        <div class="limit-malware">
          <span>VPN</span>
          <b>→</b>
          <div class="limit-file">
            <strong>!</strong>
            <small>.exe</small>
          </div>
        </div>
        <h3>Заменить антивирус</h3>
        <p>VPN не обезвреживает вирусы, вредоносные файлы и фишинговые сайты.</p>
      </div>
      <div class="limit-item">
        <div class="limit-trust">
          <div>
            <span>ISP</span>
            <small>доверие</small>
          </div>
          <b>→</b>
          <div>
            <span>VPN</span>
            <small>доверие</small>
          </div>
        </div>
        <h3>Устранить доверие</h3>
        <p>При коммерческом VPN часть доверия переносится с провайдера на VPN-сервис.</p>
      </div>
    </div>
  </div>
  <p class="limits-conclusion">VPN — инструмент защиты канала связи, а не универсальное средство безопасности и анонимности.</p>
</div>

---
<div class="security-slide">
  <div class="slide-heading">
    <span>10</span>
    <span>БЕЗОПАСНОСТЬ</span>
  </div>
  <h1>Как выбрать безопасный VPN?</h1>
  <div class="security-grid">
    <div class="security-card">
      <span>01</span>
      <h3>Репутация</h3>
      <p>Важно понимать, кто управляет VPN-сервисом и насколько прозрачно он сообщает о своей работе.</p>
    </div>
    <div class="security-card">
      <span>02</span>
      <h3>Конфиденциальность</h3>
      <p>Стоит проверить, какие данные сервис собирает, зачем они нужны и как долго хранятся.</p>
    </div>
    <div class="security-card">
      <span>03</span>
      <h3>Современные протоколы</h3>
      <p>Предпочтительны WireGuard, OpenVPN и IPsec/IKEv2 вместо устаревших решений.</p>
    </div>
    <div class="security-card security-card-accent">
      <span>04</span>
      <h3>Обновления и MFA</h3>
      <p>Обновления исправляют уязвимости, а многофакторная аутентификация дополнительно защищает доступ.</p>
    </div>
  </div>
</div>


---

<div class="conclusion-slide">
  <div class="slide-heading">
    <span>11</span>
    <span>ЗАКЛЮЧЕНИЕ</span>
  </div>
  <h1>Главное о VPN</h1>
  <div class="conclusion-grid">
    <div class="conclusion-item">
      <span>01</span>
      <h3>Защищает соединение</h3>
      <p>VPN создаёт зашифрованный туннель между устройством пользователя и VPN-сервером.</p>
    </div>
    <div class="conclusion-item conclusion-item-accent">
      <span>02</span>
      <h3>Решает разные задачи</h3>
      <p>Удалённый доступ, объединение корпоративных сетей и изменение точки выхода в интернет.</p>
    </div>
    <div class="conclusion-item">
      <span>03</span>
      <h3>Не защищает от всего</h3>
      <p>VPN не обеспечивает полную анонимность и не заменяет другие средства информационной безопасности.</p>
    </div>
  </div>
</div>

---
<div class="thanks-slide">
  <div class="thanks-content">
    <h1>Спасибо за внимание!</h1>
  </div>
</div>