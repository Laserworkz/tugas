<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Tabel Produk dengan Form Input</title>
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet" />
  <style>
    body {
      background-color: #fdfdfd;
      padding: 30px;
    }

    .section-wrapper {
      background-color: #ffffff;
      padding: 25px;
      border-radius: 15px;
      box-shadow: 0 4px 12px rgba(0, 0, 0, 0.05);
      height: 100%;
    }

    .table thead {
      background-color: #e0f7fa;
    }

    .table thead th {
      color: #00796b;
    }

    .table tbody tr:nth-child(even) {
      background-color: #f1f8e9;
    }

    .table tbody tr:nth-child(odd) {
      background-color: #f9fbe7;
    }

    .section-title {
      margin-bottom: 1.5rem;
      color: #4a5568;
    }

    .row-gap {
      row-gap: 2rem;
    }

    .title-row {
      display: flex;
      justify-content: space-between;
      align-items: center;
    }

    .delete-btn, .edit-btn {
      margin-top: 10px;
    }

    .delete-btn {
      color: red;
    }

    .edit-btn {
      color: orange;
    }

    @media (max-width: 768px) {
      .section-wrapper {
        padding: 15px;
      }
    }
  </style>
</head>
<body>
  <div class="container">
    <div class="row row-gap">
      <!-- Tabel -->
      <div class="col-md-7">
        <div class="section-wrapper">
          <div class="title-row">
            <h2 class="section-title">Daftar Produk</h2>
            <button type="button" class="btn btn-primary" data-bs-toggle="modal" data-bs-target="#productModal">
              Tambah Produk
            </button>
          </div>
          <table class="table table-bordered table-hover" id="dataTable">
            <thead>
              <tr>
                <th>No</th>
                <th>Produk</th>
                <th>Jumlah</th>
                <th>Deadline</th>
              </tr>
            </thead>
            <tbody>
              <!-- Data akan ditambahkan melalui form -->
            </tbody>
          </table>
        </div>
      </div>

      <!-- Panel Keterangan -->
      <div class="col-md-5">
        <div class="section-wrapper" id="detailPanel">
          <h4 class="section-title">Keterangan Data</h4>
          <p>Klik salah satu baris pada tabel untuk melihat detail di sini.</p>
        </div>
      </div>
    </div>

    <!-- Modal Form Input Data -->
    <div class="modal fade" id="productModal" tabindex="-1" aria-labelledby="productModalLabel" aria-hidden="true">
      <div class="modal-dialog">
        <div class="modal-content">
          <div class="modal-header">
            <h5 class="modal-title" id="productModalLabel">Form Tambah Produk</h5>
            <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
          </div>
          <div class="modal-body">
            <form id="productForm">
              <div class="mb-3">
                <label for="produk" class="form-label">Produk</label>
                <input type="text" class="form-control" id="produk" required />
              </div>
              <div class="mb-3">
                <label for="jumlah" class="form-label">Jumlah</label>
                <input type="number" class="form-control" id="jumlah" required />
              </div>
              <div class="mb-3">
                <label for="deadline" class="form-label">Deadline</label>
                <input type="date" class="form-control" id="deadline" required />
              </div>
              <div class="mb-3">
                <label for="keterangan" class="form-label">Keterangan</label>
                <textarea class="form-control" id="keterangan" rows="3" required></textarea>
              </div>
              <button type="submit" class="btn btn-primary">Simpan</button>
            </form>
          </div>
        </div>
      </div>
    </div>
  </div>

  <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"></script>
  <script>
    let selectedRow = null; // Untuk menyimpan baris yang dipilih
    let isEditing = false; // Menandakan apakah kita sedang dalam mode edit

    // Menambahkan data baru ke tabel dan ke panel keterangan
    document.getElementById('productForm').addEventListener('submit', function(e) {
      e.preventDefault(); // Mencegah form untuk refresh halaman

      // Ambil data dari form
      const produk = document.getElementById('produk').value;
      const jumlah = document.getElementById('jumlah').value;
      const deadline = document.getElementById('deadline').value;
      const keterangan = document.getElementById('keterangan').value;

      // Jika sedang dalam mode edit, perbarui data
      if (isEditing && selectedRow) {
        selectedRow.cells[1].textContent = produk;
        selectedRow.cells[2].textContent = jumlah;
        selectedRow.cells[3].textContent = deadline;
        selectedRow.setAttribute('data-detail', JSON.stringify({ produk, jumlah, deadline, keterangan }));

        // Perbarui panel keterangan
        document.getElementById('detailPanel').innerHTML = `
          <h4 class="section-title">Keterangan Data</h4>
          <p><strong>Produk:</strong> ${produk}</p>
          <p><strong>Jumlah:</strong> ${jumlah}</p>
          <p><strong>Deadline:</strong> ${deadline}</p>
          <p><strong>Keterangan:</strong><br>${keterangan}</p>
          <button class="btn btn-danger delete-btn" onclick="hapusData()">Hapus</button>
          <button class="btn btn-warning edit-btn" onclick="editData()">Edit</button>
        `;

        // Reset status edit dan baris yang dipilih
        isEditing = false;
      } else {
        // Menambahkan baris baru ke tabel
        const tableBody = document.querySelector('#dataTable tbody');
        const newRow = document.createElement('tr');
        newRow.setAttribute('data-detail', JSON.stringify({ produk, jumlah, deadline, keterangan }));

        newRow.innerHTML = `
          <td>${tableBody.rows.length + 1}</td>
          <td>${produk}</td>
          <td>${jumlah}</td>
          <td>${deadline}</td>
        `;

        // Tambahkan baris ke tabel
        tableBody.appendChild(newRow);

        // Menambahkan event listener untuk menampilkan keterangan ketika baris diklik
        newRow.addEventListener('click', () => {
          selectedRow = newRow; // Simpan baris yang dipilih
          document.getElementById('detailPanel').innerHTML = `
            <h4 class="section-title">Keterangan Data</h4>
            <p><strong>Produk:</strong> ${produk}</p>
            <p><strong>Jumlah:</strong> ${jumlah}</p>
            <p><strong>Deadline:</strong> ${deadline}</p>
            <p><strong>Keterangan:</strong><br>${keterangan}</p>
            <button class="btn btn-danger delete-btn" onclick="hapusData()">Hapus</button>
            <button class="btn btn-warning edit-btn" onclick="editData()">Edit</button>
          `;
        });
      }

      // Tutup modal setelah data disubmit
      const modal = bootstrap.Modal.getInstance(document.getElementById('productModal'));
      modal.hide();

      // Reset form setelah pengisian
      document.getElementById('productForm').reset();
    });

    // Fungsi untuk menghapus data yang dipilih
    function hapusData() {
      if (selectedRow) {
        // Hapus baris dari tabel
        selectedRow.remove();
        // Kosongkan panel keterangan
        document.getElementById('detailPanel').innerHTML = `
          <h4 class="section-title">Keterangan Data</h4>
          <p>Klik salah satu baris pada tabel untuk melihat detail di sini.</p>
        `;
        selectedRow = null; // Reset baris yang dipilih
      }
    }

    // Fungsi untuk mengedit data yang dipilih
    function editData() {
      if (selectedRow) {
        const dataDetail = JSON.parse(selectedRow.getAttribute('data-detail'));
        document.getElementById('produk').value = dataDetail.produk;
        document.getElementById('jumlah').value = dataDetail.jumlah;
        document.getElementById('deadline').value = dataDetail.deadline;
        document.getElementById('keterangan').value = dataDetail.keterangan;

        // Ubah status menjadi edit
        isEditing = true;

        // Buka modal untuk mengedit
        const modal = new bootstrap.Modal(document.getElementById('productModal'));
        modal.show();
      }
    }

    // Fungsi untuk menampilkan konfirmasi sebelum menghapus data
function hapusData() {
  if (selectedRow) {
    // Menampilkan konfirmasi sebelum menghapus
    const confirmDelete = confirm("Apakah Anda yakin ingin menghapus data ini?");
    if (confirmDelete) {
      // Jika pengguna mengonfirmasi, hapus data
      selectedRow.remove();
      // Kosongkan panel keterangan
      document.getElementById('detailPanel').innerHTML = `
        <h4 class="section-title">Keterangan Data</h4>
        <p>Klik salah satu baris pada tabel untuk melihat detail di sini.</p>
      `;
      selectedRow = null; // Reset baris yang dipilih
    }
  }
}

  </script>
</body>
</html>
