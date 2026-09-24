<script setup>
function kirimPesan(event) {
  event.preventDefault();

  alert("Pesan berhasil dikirim!");

  window.location.reload();
}
</script>

<template>
  <main class="contact-page">
    <!-- JUDUL -->
    <section class="judul">
      <div class="judul-content">
        <span class="icon">💬</span>

        <h1>Kontak Kami</h1>

        <p>Ada pertanyaan? Jangan ragu untuk menghubungi kami.</p>
      </div>
    </section>

    <!-- KONTEN -->
    <section class="contact-container">
      <!-- KIRI -->
      <div class="info-kontak">
        <h2>📞 Informasi Kontak</h2>

        <p class="deskripsi">
          Silakan hubungi kami melalui informasi di bawah ini. Kami siap
          membantu memberikan informasi mengenai produk dan layanan online shop
          sekolah.
        </p>

        <!-- ALAMAT -->
        <div class="info-box">
          <div class="info-icon alamat">📍</div>

          <div>
            <h3>Alamat</h3>
            <p>Jalan sini deket situ</p>
          </div>
        </div>

        <!-- TELEPON -->
        <div class="info-box">
          <div class="info-icon telepon">📱</div>

          <div>
            <h3>Telepon</h3>
            <p>(+62) 89555532444</p>
          </div>
        </div>

        <!-- EMAIL -->
        <div class="info-box">
          <div class="info-icon email">✉️</div>

          <div>
            <h3>Email</h3>
            <p>smkyadikasoreang@gmail.com</p>
          </div>
        </div>

        <!-- CARD TAMBAHAN -->
        <div class="school-card">
          <h3>🎓 SMK YADIKA SOREANG</h3>

          <p>Belanja gampang, sekolah senang!</p>
        </div>
      </div>

      <!-- KANAN -->
      <div class="form-kontak">
        <h2>✉️ Kirim Pesan</h2>

        <p class="deskripsi">
          Isi formulir di bawah ini dan kirimkan pesan kepada kami.
        </p>

        <form @submit="kirimPesan">
          <!-- NAMA -->
          <div class="form-group">
            <label>Nama</label>

            <input type="text" placeholder="Masukkan nama kamu" required />
          </div>

          <!-- EMAIL -->
          <div class="form-group">
            <label>Email</label>

            <input
              type="email"
              placeholder="Masukkan email kamu"
              required
              pattern="[a-zA-Z0-9._%+-]+@gmail\.com"
              title="Email harus menggunakan @gmail.com"
            />
          </div>

          <!-- PESAN -->
          <div class="form-group">
            <label>Pesan</label>

            <textarea
              placeholder="Tulis pesan kamu di sini..."
              required
            ></textarea>
          </div>

          <!-- BUTTON -->
          <button type="submit">🚀 Kirim Pesan</button>
        </form>
      </div>
    </section>
  </main>
</template>

<style scoped>
* {
  box-sizing: border-box;
}

/* =========================
   HALAMAN
========================= */

.contact-page {
  min-height: 600px;
  background: #f4f6fb;
}

/* =========================
   JUDUL
========================= */

.judul {
  padding: 55px 20px;
  text-align: center;
  color: white;

  background: linear-gradient(135deg, #243b8f, #3f51d1, #6c4de6);
}

.judul-content {
  max-width: 800px;
  margin: auto;
}

.icon {
  display: block;
  font-size: 45px;
  margin-bottom: 10px;
}

.judul h1 {
  margin: 0;
  font-size: 42px;
  font-weight: 800;
}

.judul p {
  margin-top: 12px;
  font-size: 18px;
  color: #e5e7ff;
}

/* =========================
   CONTAINER
========================= */

.contact-container {
  max-width: 1100px;
  margin: 0 auto;

  display: grid;
  grid-template-columns: 1fr 1fr;

  gap: 35px;

  padding: 50px 25px;
}

/* =========================
   CARD KIRI & KANAN
========================= */

.info-kontak,
.form-kontak {
  background: white;

  padding: 35px;

  border-radius: 20px;

  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.08);

  transition: 0.3s;
}

.info-kontak:hover,
.form-kontak:hover {
  transform: translateY(-5px);

  box-shadow: 0 15px 35px rgba(0, 0, 0, 0.12);
}

/* =========================
   JUDUL CARD
========================= */

.info-kontak h2,
.form-kontak h2 {
  margin-top: 0;

  margin-bottom: 10px;

  font-size: 26px;

  color: #1f2937;
}

/* =========================
   DESKRIPSI
========================= */

.deskripsi {
  color: #6b7280;

  line-height: 1.7;

  margin-bottom: 25px;
}

/* =========================
   INFO BOX
========================= */

.info-box {
  display: flex;

  align-items: center;

  gap: 15px;

  padding: 15px;

  margin-bottom: 15px;

  border-radius: 14px;

  background: #f8f9ff;

  transition: 0.3s;
}

.info-box:hover {
  transform: translateX(5px);

  background: #eef1ff;
}

/* ICON */

.info-icon {
  width: 50px;
  height: 50px;

  display: flex;

  align-items: center;
  justify-content: center;

  border-radius: 12px;

  font-size: 25px;
}

/* WARNA ICON */

.alamat {
  background: #dbeafe;
}

.telepon {
  background: #dcfce7;
}

.email {
  background: #f3e8ff;
}

/* TEKS */

.info-box h3 {
  margin: 0 0 4px;

  font-size: 17px;

  color: #111827;
}

.info-box p {
  margin: 0;

  color: #6b7280;
}

/* =========================
   SCHOOL CARD
========================= */

.school-card {
  margin-top: 25px;

  padding: 20px;

  border-radius: 15px;

  color: white;

  background: linear-gradient(135deg, #2563eb, #4f46e5);
}

.school-card h3 {
  margin: 0 0 8px;

  font-size: 19px;
}

.school-card p {
  margin: 0;

  color: #dbeafe;
}

/* =========================
   FORM
========================= */

.form-group {
  margin-bottom: 20px;
}

.form-group label {
  display: block;

  margin-bottom: 8px;

  font-weight: 600;

  color: #374151;
}

.form-kontak input,
.form-kontak textarea {
  width: 100%;

  padding: 13px 15px;

  border: 1px solid #d1d5db;

  border-radius: 10px;

  font-size: 15px;

  outline: none;

  transition: 0.3s;

  font-family: inherit;
}

.form-kontak input:focus,
.form-kontak textarea:focus {
  border-color: #3b82f6;

  box-shadow: 0 0 0 3px rgba(59, 130, 246, 0.15);
}

.form-kontak textarea {
  min-height: 130px;

  resize: vertical;
}

/* =========================
   BUTTON
========================= */

.form-kontak button {
  width: 100%;

  padding: 14px;

  border: none;

  border-radius: 10px;

  background: linear-gradient(135deg, #2563eb, #4f46e5);

  color: white;

  font-size: 16px;

  font-weight: 700;

  cursor: pointer;

  transition: 0.3s;
}

.form-kontak button:hover {
  transform: translateY(-2px);

  box-shadow: 0 8px 20px rgba(37, 99, 235, 0.3);
}

/* =========================
   RESPONSIVE HP
========================= */

@media (max-width: 768px) {
  .contact-container {
    grid-template-columns: 1fr;

    padding: 30px 15px;
  }

  .judul h1 {
    font-size: 32px;
  }

  .info-kontak,
  .form-kontak {
    padding: 25px;
  }
}
</style>
