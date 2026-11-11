<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
  <title>London Day Trip</title>
  <style>
    :root {
      --bg: #0d0d0f;
      --card: #1c1c1e;
      --border: #2c2c2e;
      --text: #ffffff;
      --muted: #8e8e93;
      --accent: #0a84ff;
      --sight: #30d158;
      --food: #ff9f0a;
      --show: #bf5af2;
      --transit: #64d2ff;
    }
    * { box-sizing: border-box; margin: 0; padding: 0; font-family: -apple-system, BlinkMacSystemFont, "SF Pro Display", sans-serif; }
    body { background: var(--bg); color: var(--text); padding: 12px; max-width: 600px; margin: 0 auto; -webkit-font-smoothing: antialiased; }
    header { background: var(--card); border: 2px solid var(--border); border-radius: 16px; padding: 16px; margin-bottom: 14px; }
    h1 { font-size: 22px; font-weight: 800; color: #fff; margin-bottom: 6px; }
    .meta-line { font-size: 14px; color: var(--muted); display: flex; justify-content: space-between; font-weight: 600; }
    .day-card { background: var(--card); border: 2px solid var(--border); border-radius: 16px; padding: 16px; margin-bottom: 14px; }
    .day-title { font-size: 18px; font-weight: 800; color: var(--accent); text-transform: uppercase; letter-spacing: 0.8px; margin-bottom: 12px; padding-bottom: 8px; border-bottom: 2px solid var(--border); }
    .item-list { display: flex; flex-direction: column; gap: 10px; }
    .item { display: flex; align-items: center; gap: 10px; background: rgba(255,255,255,0.05); padding: 12px 14px; border-radius: 12px; transition: all 0.2s ease; }
    .item.completed { opacity: 0.4; text-decoration: line-through; background: rgba(255,255,255,0.02); }
    
    /* Custom Checkbox */
    .checkbox-container { display: flex; align-items: center; cursor: pointer; flex-shrink: 0; }
    .checkbox-container input { display: none; }
    .checkmark { width: 22px; height: 22px; border: 2px solid var(--border); border-radius: 6px; background: rgba(255,255,255,0.1); display: flex; align-items: center; justify-content: center; }
    .checkbox-container input:checked ~ .checkmark { background: var(--accent); border-color: var(--accent); }
    .checkmark:after { content: ""; display: none; width: 5px; height: 10px; border: solid white; border-width: 0 2px 2px 0; transform: rotate(45deg); }
    .checkbox-container input:checked ~ .checkmark:after { display: block; }
    
    .icon { font-size: 18px; width: 20px; text-align: center; flex-shrink: 0; }
    .details { flex-grow: 1; display: flex; flex-direction: column; gap: 2px; min-width: 0; }
    .name-link { font-weight: 700; color: #fff; font-size: 15px; text-decoration: underline; text-decoration-color: rgba(255,255,255,0.3); text-underline-offset: 3px; }
    .hours { font-size: 11px; color: var(--muted); font-weight: 500; }
    
    .btn-group { display: flex; gap: 6px; flex-shrink: 0; align-items: center; }
    .ticket-btn { background: rgba(255, 59, 48, 0.2); color: #ff6961; font-size: 11px; font-weight: 800; text-transform: uppercase; padding: 5px 8px; border-radius: 6px; text-decoration: none; border: 1px solid rgba(255, 59, 48, 0.4); letter-spacing: 0.5px; }
    .badge { font-size: 11px; font-weight: 800; text-transform: uppercase; padding: 5px 8px; border-radius: 6px; letter-spacing: 0.5px; }
    
    .tag-transit { background: rgba(100, 210, 255, 0.2); color: var(--transit); }
    .tag-sight { background: rgba(48, 209, 88, 0.2); color: var(--sight); }
    .tag-food { background: rgba(255, 159, 10, 0.2); color: var(--food); }
    .tag-show { background: rgba(191, 90, 242, 0.2); color: var(--show); }
  </style>
</head>
<body>

  <header>
    <h1>🇬🇧 LONDON DAY TRIP</h1>
    <div class="meta-line">
      <span>🚆 Outbound: 09:54 AM</span>
      <span>🚆 Return: 09:39 PM</span>
    </div>
  </header>

  <div class="day-card">
    <div class="day-title">Itinerary Schedule</div>
    <div class="item-list">

      <div class="item" id="item-ldn-1">
        <label class="checkbox-container">
          <input type="checkbox" onchange="toggleComplete('item-ldn-1')">
          <span class="checkmark"></span>
        </label>
        <span class="icon">🚆</span>
        <div class="details">
          <a class="name-link" href="https://www.google.com/maps/search/?api=1&query=Manchester+Piccadilly+Station" target="_blank">09:54 AM — Train to London</a>
          <span class="hours">Arrive London Euston at 12:05 PM</span>
        </div>
        <span class="badge tag-transit">Train</span>
      </div>

      <div class="item" id="item-ldn-2">
        <label class="checkbox-container">
          <input type="checkbox" onchange="toggleComplete('item-ldn-2')">
          <span class="checkmark"></span>
        </label>
        <span class="icon">🐟</span>
        <div class="details">
          <a class="name-link" href="https://www.google.com/maps/search/?api=1&query=Hobson%27s+Fish+%26+Chips+London" target="_blank">Hobson’s Fish & Chips</a>
          <span class="hours">Open: 12:00 – 22:00</span>
        </div>
        <span class="badge tag-food">Food</span>
      </div>

      <div class="item" id="item-ldn-3">
        <label class="checkbox-container">
          <input type="checkbox" onchange="toggleComplete('item-ldn-3')">
          <span class="checkmark"></span>
        </label>
        <span class="icon">🥩</span>
        <div class="details">
          <a class="name-link" href="https://www.google.com/maps/search/?api=1&query=The+Quality+Chop+House+London" target="_blank">Quality Chop House</a>
          <span class="hours">Open: 12:00 – 23:00</span>
        </div>
        <span class="badge tag-food">Food</span>
      </div>

      <div class="item" id="item-ldn-4">
        <label class="checkbox-container">
          <input type="checkbox" onchange="toggleComplete('item-ldn-4')">
          <span class="checkmark"></span>
        </label>
        <span class="icon">🍫</span>
        <div class="details">
          <a class="name-link" href="https://www.google.com/maps/search/?api=1&query=Pierre+Marcolini+London" target="_blank">Pierre Marcolini</a>
          <span class="hours">Open: 11:00 – 20:00</span>
        </div>
        <span class="badge tag-food">Shop</span>
      </div>

      <div class="item" id="item-ldn-5">
        <label class="checkbox-container">
          <input type="checkbox" onchange="toggleComplete('item-ldn-5')">
          <span class="checkmark"></span>
        </label>
        <span class="icon">🎭</span>
        <div class="details">
          <a class="name-link" href="https://www.google.com/maps/search/?api=1&query=London+County+Hall+Witness+for+the+Prosecution" target="_blank">02:30 PM — Witness for the Prosecution</a>
          <span class="hours">Showtime: 14:30 – 17:00 @ London County Hall</span>
        </div>
        <div class="btn-group">
          <a class="ticket-btn" href="https://ticketing.kxtickets.com/shop/tickets/bundle/60a978fa-7e4e-4ec5-84bf-e298d67825c4/event/2001384" target="_blank">Ticket</a>
          <span class="badge tag-show">Show</span>
        </div>
      </div>

      <div class="item" id="item-ldn-6">
        <label class="checkbox-container">
          <input type="checkbox" onchange="toggleComplete('item-ldn-6')">
          <span class="checkmark"></span>
        </label>
        <span class="icon">🎁</span>
        <div class="details">
          <a class="name-link" href="https://www.google.com/maps/search/?api=1&query=Fortnum+%26+Mason+London" target="_blank">Fortnum & Mason</a>
          <span class="hours">Christmas Lights Route</span>
        </div>
        <span class="badge tag-sight">Sight</span>
      </div>

      <div class="item" id="item-ldn-7">
        <label class="checkbox-container">
          <input type="checkbox" onchange="toggleComplete('item-ldn-7')">
          <span class="checkmark"></span>
        </label>
        <span class="icon">🎄</span>
        <div class="details">
          <a class="name-link" href="https://www.google.com/maps/search/?api=1&query=Regent+Street+London" target="_blank">Regent Street</a>
          <span class="hours">Christmas Lights Route</span>
        </div>
        <span class="badge tag-sight">Sight</span>
      </div>

      <div class="item" id="item-ldn-8">
        <label class="checkbox-container">
          <input type="checkbox" onchange="toggleComplete('item-ldn-8')">
          <span class="checkmark"></span>
        </label>
        <span class="icon">✨</span>
        <div class="details">
          <a class="name-link" href="https://www.google.com/maps/search/?api=1&query=Carnaby+Street+London" target="_blank">Carnaby Street</a>
          <span class="hours">Christmas Lights Route</span>
        </div>
        <span class="badge tag-sight">Sight</span>
      </div>

      <div class="item" id="item-ldn-9">
        <label class="checkbox-container">
          <input type="checkbox" onchange="toggleComplete('item-ldn-9')">
          <span class="checkmark"></span>
        </label>
        <span class="icon">🚆</span>
        <div class="details">
          <a class="name-link" href="https://www.google.com/maps/search/?api=1&query=Euston+Station+London" target="_blank">09:39 PM — Train to Manchester</a>
          <span class="hours">Depart London Euston Station</span>
        </div>
        <span class="badge tag-transit">Train</span>
      </div>

    </div>
  </div>

  <script>
    function toggleComplete(id) {
      const el = document.getElementById(id);
      const checkbox = el.querySelector('input[type="checkbox"]');
      if (checkbox.checked) {
        el.classList.add('completed');
        localStorage.setItem(id, 'true');
      } else {
        el.classList.remove('completed');
        localStorage.setItem(id, 'false');
      }
    }

    // Load saved states
    window.addEventListener('DOMContentLoaded', () => {
      document.querySelectorAll('.item').forEach(item => {
        const id = item.id;
        const saved = localStorage.getItem(id);
        if (saved === 'true') {
          item.classList.add('completed');
          const checkbox = item.querySelector('input[type="checkbox"]');
          if (checkbox) checkbox.checked = true;
        }
      });
    });
  </script>
</body>
</html>
