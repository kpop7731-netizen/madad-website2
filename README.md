<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>مِداد | الشاب المسلم</title>
<link href="https://fonts.googleapis.com/css2?family=Amiri:wght@400;700&family=Aref+Ruqaa:wght@400;700&display=swap" rel="stylesheet">
<style>
  * { box-sizing: border-box; margin: 0; padding: 0; }
  body {
    background: #0D0B08;
    font-family: 'Amiri', serif;
    color: #EDE6D6;
    line-height: 1.8;
  }
  
  header {
    text-align: center;
    padding: 40px 20px 20px;
    border-bottom: 0.5px solid #2A2419;
  }
  .brand {
    font-family: 'Aref Ruqaa', serif;
    font-size: 48px;
    color: #C9A24B;
    margin-bottom: 4px;
  }
  .sub-brand {
    font-size: 14px;
    color: #A69B7E;
    letter-spacing: 3px;
  }

  .container {
    max-width: 800px;
    margin: 0 auto;
    padding: 32px 20px;
  }

  .hero-quote {
    text-align: center;
    margin: 30px 0 40px;
    padding: 24px;
    background: rgba(201, 162, 75, 0.05);
    border-right: 3px solid #C9A24B;
    border-left: 3px solid #C9A24B;
    border-radius: 8px;
  }
  .hero-quote p {
    font-size: 22px;
    font-weight: 700;
    color: #C9A24B;
    line-height: 1.6;
  }
  .hero-quote span {
    display: block;
    margin-top: 10px;
    font-size: 14px;
    color: #A69B7E;
    font-weight: normal;
  }

  .video-section {
    margin: 40px 0;
    text-align: center;
  }
  .video-container {
    position: relative;
    padding-bottom: 56.25%; /* 16:9 Aspect Ratio */
    height: 0;
    overflow: hidden;
    border-radius: 12px;
    border: 1px solid #3A311F;
    box-shadow: 0 10px 30px rgba(0,0,0,0.7);
  }
  .video-container iframe {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    border: 0;
  }

  /* Booking Form Card Section */
  .booking-section {
    display: flex;
    justify-content: center;
    margin: 50px 0 30px;
  }
  .card {
    width: 100%;
    max-width: 480px;
    background: linear-gradient(160deg, #16130F, #1E1812);
    border: 0.5px solid #3A311F;
    border-radius: 14px;
    padding: 32px 26px;
    box-shadow: 0 10px 30px rgba(0,0,0,0.5);
  }
  .card h2 {
    text-align: center;
    font-size: 30px;
    font-weight: 700;
    color: #C9A24B;
    margin: 0 0 4px;
  }
  .card .tagline {
    text-align: center;
    font-size: 13px;
    color: #A69B7E;
    letter-spacing: 2px;
    margin: 0 0 22px;
  }
  .counter {
    text-align: center;
    background: rgba(201,162,75,0.08);
    border: 0.5px solid rgba(201,162,75,0.3);
    border-radius: 10px;
    padding: 10px;
    margin-bottom: 22px;
    font-size: 14px;
    color: #EDE6D6;
  }
  .counter b { color: #C9A24B; font-size: 16px; }
  label {
    display: block;
    font-size: 13px;
    color: #B9AF98;
    margin: 14px 0 6px;
  }
  input, select, textarea {
    width: 100%;
    background: #0D0B08;
    border: 0.5px solid #3A311F;
    border-radius: 8px;
    color: #EDE6D6;
    font-family: 'Amiri', serif;
    font-size: 14px;
    padding: 10px 12px;
  }
  input:focus, select:focus, textarea:focus {
    outline: none;
    border-color: #C9A24B;
  }
  .custom-qty-container {
    display: none;
    margin-top: 8px;
  }
  .price-container {
    margin: 20px 0 6px;
    background: rgba(201,162,75,0.04);
    border: 0.5px dashed rgba(201,162,75,0.25);
    border-radius: 8px;
    padding: 12px 14px;
  }
  .launch-badge {
    display: inline-block;
    background: #C9A24B;
    color: #0D0B08;
    font-size: 11px;
    font-weight: bold;
    padding: 2px 8px;
    border-radius: 4px;
    margin-bottom: 8px;
  }
  .price-row {
    display: flex;
    justify-content: space-between;
    align-items: center;
    font-size: 13px;
    color: #B9AF98;
  }
  .price-row b { color: #C9A24B; font-size: 20px; }
  .shipping-note {
    font-size: 11px;
    color: #A69B7E;
    text-align: right;
    margin-top: 6px;
    line-height: 1.5;
  }
  .price-increase-warning {
    color: #E27878;
    font-size: 11px;
    margin-top: 4px;
  }
  .err {
    color: #E27878;
    font-size: 12px;
    margin-top: 4px;
    display: none;
  }
  button {
    width: 100%;
    margin-top: 22px;
    background: #C9A24B;
    color: #0D0B08;
    border: none;
    border-radius: 8px;
    font-family: 'Amiri', serif;
    font-weight: 700;
    font-size: 16px;
    padding: 13px;
    cursor: pointer;
    transition: background 0.2s;
  }
  button:hover { background: #d8b056; }
  button:active { opacity: 0.85; }
  .confirm {
    display: none;
    text-align: center;
    margin-top: 18px;
    font-size: 14px;
    color: #C9A24B;
    line-height: 1.8;
  }
  .note {
    text-align: center;
    font-size: 11px;
    color: #6B6355;
    margin-top: 16px;
  }

  footer {
    text-align: center;
    padding: 30px 20px;
    font-size: 12px;
    color: #6B6355;
    border-top: 0.5px solid #2A2419;
    margin-top: 40px;
  }
  footer a {
    color: #C9A24B;
    text-decoration: none;
    margin: 0 8px;
  }
</style>
</head>
<body>

<header>
  <div class="brand">مِداد</div>
  <div class="sub-brand">الشاب المسلم</div>
</header>

<div class="container">

  <!-- قسم العبارة التسويقية الجذابة -->
  <div class="hero-quote">
    <p>«ليس الإنجاز مجرد أن تخطط ليومك... بل كيف تحوّل كل سعيٍ وحركةٍ فيه إلى عبادة بالنية»</p>
    <span>مخطط يومي مصمم بعناية ليصحبك في رحلة التزكية وإدارة الوقت والتخطيط الإيماني.</span>
  </div>

  <!-- قسم فيديو اليوتيوب المدمج -->
  <div class="video-section">
    <div class="video-container">
      <iframe src="https://www.youtube.com/embed/Zzc_FN3J3d0" title="قصة مِداد... الرفيق اليومي للشاب المسلم بعيدًا عن شاشة الهاتف" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
    </div>
  </div>

  <!-- قسم كود الحجز والدفع -->
  <div class="booking-section" id="booking">
    <div class="card">
      <h2>مِداد</h2>
      <p class="tagline">الشاب المسلم</p>

      <div class="counter" id="counterBox">
        متبقي <b id="remaining">…</b> من ٥٠ نسخة من دفعة الإطلاق
      </div>

      <form id="bookingForm">
        <label for="name">الاسم بالكامل</label>
        <input type="text" id="name" placeholder="اكتب اسمك هنا">
        <div class="err" id="nameErr">من فضلك اكتب اسمك</div>

        <label for="phone">رقم الواتساب للتواصل والتأكيد</label>
        <input type="tel" id="phone" placeholder="01xxxxxxxxx">
        <div class="err" id="phoneErr">من فضلك اكتب رقم هاتف صحيح</div>

        <label for="qty">عدد النسخ المطلوبة</label>
        <select id="qty">
          <option value="1">نسخة واحدة</option>
          <option value="2">نسختان</option>
          <option value="3">٣ نسخ</option>
          <option value="more">أكثر من ذلك (اكتب العدد)</option>
        </select>

        <div class="custom-qty-container" id="customQtyBox">
          <label for="customQty">حدد عدد النسخ المطلوبة:</label>
          <input type="number" id="customQty" min="4" value="4" placeholder="أدخل العدد">
        </div>

        <label for="notes">العنوان أو الملاحظات (اختياري)</label>
        <textarea id="notes" rows="2" placeholder="المحافظة / العنوان / وقت مناسب للتواصل..."></textarea>

        <div class="price-container">
          <span class="launch-badge" id="launchBadge">عرض الإطلاق الحصري 🔥</span>
          <div class="price-row">
            <span>السعر الإجمالي:</span>
            <b id="totalPrice">١٠٠ ج.م</b>
          </div>
          <div class="shipping-note">* السعر لا يشمل مصاريف الشحن</div>
          <div class="price-increase-warning" id="priceWarning">⚠️ هذا السعر خاص بـ ٥٠ نسخة الأولى فقط، وسيرتفع السعر بعد انتهاء دفعة الإطلاق.</div>
        </div>

        <button type="submit" id="submitBtn">احجز نسختك بسعر الإطلاق الآن</button>
      </form>

      <div class="confirm" id="confirmMsg">
        تم فتح تطبيق الواتساب لإرسال الطلب ✅<br>
        إذا لم يفتح تلقائياً، يمكنك التواصل مباشرة على:<br>
        <b style="color:#EDE6D6; direction:ltr; display:inline-block;">+201556518997</b>
      </div>

      <p class="note">بياناتك تُرسل مباشرة عبر حسابك على واتساب بخصوصية تامة.</p>
    </div>
  </div>

</div>

<footer>
  <p>© جميع الحقوق محفوظة لمشروع مِداد - الشاب المسلم</p>
</footer>

<script>
// ==========================================
const OWNER_WHATSAPP = "201556518997"; 
const GOOGLE_FORM_URL = "https://docs.google.com/forms/d/e/1FAIpQLSdNahrkkdRIs0PqiaiL1uAfmML8s3uqE35MVlGakPGU1dHutA/formResponse";
const APPS_SCRIPT_URL = "https://script.google.com/macros/s/AKfycbzaoJcSkUTzUPztp7nPEHWHzj970Zypwi7bwy5TshmTKAlRBBcreuRdR7B0GLvA8ZUthQ/exec";

const ENTRY_NAME = "entry.1250543120";
const ENTRY_PHONE = "entry.2075273833";
const ENTRY_QTY = "entry.1807369720";
const ENTRY_NOTES = "entry.418540168";
// ==========================================

const LAUNCH_PRICE = 100;
const REGULAR_PRICE = 150;
const TOTAL_COPIES = 50;

let currentUnitPrice = LAUNCH_PRICE;
let isLaunchEnded = false;

// جلب العدد المباع وتطبيق التحول الآلي
async function fetchRemainingFromSheet() {
  try {
    const res = await fetch(APPS_SCRIPT_URL);
    const data = await res.json();
    const sold = data.totalSold || 0;
    const remaining = Math.max(TOTAL_COPIES - sold, 0);

    if (sold >= TOTAL_COPIES) {
      // انتهت دفعة الإطلاق
      isLaunchEnded = true;
      currentUnitPrice = REGULAR_PRICE;
      
      document.getElementById('counterBox').innerHTML = "تم بيع <b>" + sold + "</b> نسخة حتى الآن";
      document.getElementById('launchBadge').textContent = "السعر الرسمي";
      document.getElementById('priceWarning').style.display = 'none';
      document.getElementById('submitBtn').textContent = "احجز نسختك الآن";
    } else {
      // لا تزال دفعة الإطلاق مستمرة
      isLaunchEnded = false;
      currentUnitPrice = LAUNCH_PRICE;
      
      document.getElementById('counterBox').innerHTML = 'متبقي <b id="remaining">' + remaining + '</b> من ٥٠ نسخة من دفعة الإطلاق';
      document.getElementById('launchBadge').textContent = "عرض الإطلاق الحصري 🔥";
      document.getElementById('priceWarning').style.display = 'block';
      document.getElementById('submitBtn').textContent = "احجز نسختك بسعر الإطلاق الآن";
    }
    
    updateTotalPrice();
  } catch (err) {
    console.error("خطأ في جلب العداد:", err);
  }
}

function getSelectedQty() {
  const qtySelect = document.getElementById('qty').value;
  if (qtySelect === 'more') {
    const customVal = parseInt(document.getElementById('customQty').value, 10);
    return isNaN(customVal) || customVal < 1 ? 1 : customVal;
  }
  return parseInt(qtySelect, 10);
}

function updateTotalPrice() {
  const qty = getSelectedQty();
  const total = qty * currentUnitPrice;
  document.getElementById('totalPrice').textContent = total + " ج.م";
}

document.getElementById('qty').addEventListener('change', function() {
  const customBox = document.getElementById('customQtyBox');
  if (this.value === 'more') {
    customBox.style.display = 'block';
  } else {
    customBox.style.display = 'none';
  }
  updateTotalPrice();
});

document.getElementById('customQty').addEventListener('input', updateTotalPrice);

fetchRemainingFromSheet();

document.getElementById('bookingForm').addEventListener('submit', function(e) {
  e.preventDefault();

  const name = document.getElementById('name').value.trim();
  const phone = document.getElementById('phone').value.trim();
  const qty = getSelectedQty();
  const notes = document.getElementById('notes').value.trim();

  const nameErr = document.getElementById('nameErr');
  const phoneErr = document.getElementById('phoneErr');
  nameErr.style.display = 'none';
  phoneErr.style.display = 'none';

  let valid = true;
  if (!name) { nameErr.style.display = 'block'; valid = false; }
  if (!phone || phone.length < 8) { phoneErr.style.display = 'block'; valid = false; }
  if (!valid) return;

  const formBody = new URLSearchParams();
  formBody.append(ENTRY_NAME, name);
  formBody.append(ENTRY_PHONE, phone);
  formBody.append(ENTRY_QTY, qty);
  formBody.append(ENTRY_NOTES, notes);

  fetch(GOOGLE_FORM_URL, {
    method: 'POST',
    mode: 'no-cors',
    headers: { 'Content-Type': 'application/x-www-form-urlencoded' },
    body: formBody
  }).then(() => {
    setTimeout(fetchRemainingFromSheet, 3000);
  }).catch(err => console.log(err));

  const total = qty * currentUnitPrice;
  let message = isLaunchEnded 
    ? "السلام عليكم، أرغب في حجز نسخة من مشروع (مداد | الشاب المسلم)\n\n"
    : "السلام عليكم، أرغب في حجز نسخة بسعر الإطلاق من مشروع (مداد | الشاب المسلم)\n\n";

  message += "👤 الاسم: " + name + "\n";
  message += "📞 رقم التواصل: " + phone + "\n";
  message += "📚 عدد النسخ: " + qty + "\n";
  message += "💰 الإجمالي: " + total + " جنيه مصري (غير شامل الشحن)\n";
  if (notes) message += "📝 ملاحظات/العنوان: " + notes + "\n";

  const waLink = "https://wa.me/" + OWNER_WHATSAPP + "?text=" + encodeURIComponent(message);
  window.open(waLink, '_blank');

  document.getElementById('confirmMsg').style.display = 'block';
  document.getElementById('bookingForm').reset();
  document.getElementById('customQtyBox').style.display = 'none';
  updateTotalPrice();
});
</script>
</body>
</html>
