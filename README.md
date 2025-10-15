Bu repozitoriy KetmonShop uchun ochilgan public landing page (mahsulot sahifalari) to'plamidir. Har bir landing page lokal HTML fayl bo'lib, rasmiy KetmonShop mahsulot sahifasiga yo'naltiradi.

**Development version:** [https://ketmonshopuz.web.app](https://ketmonshopuz.web.app)

Qoidalar va talablar
1. Texnologiyalar:
	- Landing sahifalar HTML, CSS, JavaScript yoki Tailwind CSS yordamida yaratilishi mumkin.

2. Tashqi havolalar:
	- Sahifalar faqat va faqat ketmonshop.uz domeniga yoki lokal fayllarga havola qilishi mumkin.
	- Boshqa saytlar yoki manbalarga tashqi linklar man etiladi.

3. Narx:
	- Landing sahifalarda narx (price) ko'rsatilmaydi. Narx va mavjudlik to'g'risidagi ma'lumotlar rasmiy mahsulot sahifasiga bog'lanadi.

4. Konversiya va SEO:
	- Sahifalar konversiyani oshirishga yo'naltirilgan usullarni qo'llashi kerak (aniq CTA, ijtimoiy isbot yoki qisqa ijtimoiy dalillar, o'qish uchun sodda va ishontiruvchi nusxa).
	- Har bir sahifa Open Graph va Twitter Card meta teglarini o'z ichiga olishi kerak.
	- Har bir sahifa JSON-LD (schema.org Product) yoki tegishli strukturalangan ma'lumotni qo'llashi tavsiya etiladi (price bo'lmasa ham offers.url bo'lishi mumkin).

5. Formalar:
	- Barcha kontakt yoki buyurtma shakllari quyidagi manzilga POST orqali yuborilishi kerak:
	  - action: https://ketmonshop.uz/send.php
	  - method: POST
	- Formalar quyidagi maydonlarni yuborishi shart:
	  - offer_id (mahsulot identifikatori)
	  - phone
	  - name
	- Ixtiyoriy: referrer_input maydoni (agar sahifa JavaScript orqali referer oladigan bo'lsa) — lekin bu majburiy emas.

	- Tavsiya: telefon maydoni uchun input mask qo'llash tavsiya etiladi (masalan, Inputmask.js yoki intl-tel-input). Bu foydalanuvchilarga telefon raqamlarini standart formatda kiritishga yordam beradi va server tomonida validatsiyani soddalashtiradi.

6. Canonical:
	- Har bir sahifa canonical tegida ketmonshop.github.com domenidagi sahifa versiyasiga ishora qilishi kerak. Masalan:
	  <link rel="canonical" href="https://ketmonshop.github.com/products/olmas-umarbekov-odam-bolish-qiyin.html">

7. Boshqa talablar:
	- Sahifalar SEO va konversiya uchun optimallashtirilgan bo'lishi kerak (meta description, title, og: teglar, toza URL, tez yuklanadigan rasm va minimal JS).
	- Sahifalar rasmiy mahsulot sahifasiga aniq CTA bilan yo'naltirishi kerak.

8. Barcha landing sahifalar unikal bo'lishi kerak

9. Barcha landing sahifalar yaratilganidan keyin index.html sahifasida unga havola qo'shish kerak

10. Barcha landing sahifalarni AMP versiyalari bo'lishi kerak

Namuna forma (HTML):
<form action="https://ketmonshop.uz/send.php" method="POST">
  <input type="hidden" name="offer_id" value="2348">
  <input type="text" name="name" placeholder="Ismingiz">
  <input type="tel" name="phone" placeholder="Telefon raqamingiz">
  <!-- optional: <input type="hidden" name="referrer_input" value="..."> -->
  <button type="submit">Buyurtma berish</button>
</form>

Iltimos, barcha yangi landing sahifalarni ushbu qo'llanmaga muvofiq yarating

![ketmonshop logo](ketmonshop_logo.jpg)
