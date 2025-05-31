# Bookshelf API

Bookshelf API adalah sebuah RESTful API yang dibangun menggunakan Hapi Framework untuk mengelola data buku. API ini memungkinkan pengguna untuk melakukan operasi CRUD (Create, Read, Update, Delete) pada data buku.

## Fitur

- Menambahkan buku baru
- Menampilkan seluruh buku
- Menampilkan detail buku
- Mengubah data buku
- Menghapus buku
- Filter buku berdasarkan nama, status membaca, dan status selesai

## Teknologi yang Digunakan

- Node.js
- Hapi Framework
- Nanoid (untuk generate ID)

## Persyaratan

- Node.js (versi 14 atau lebih tinggi)
- NPM (Node Package Manager)

## Instalasi

1. Clone repository ini

   ```bash
   git clone [https://github.com/mridho24/BookShelf.git]
   ```

2. Masuk ke direktori proyek

   ```bash
   cd bookshelf-api
   ```

3. Install dependencies

   ```bash
   npm install
   ```

4. Jalankan server
   ```bash
   npm run start
   ```

Server akan berjalan pada `http://localhost:9000`

## Penggunaan API

### 1. Menambahkan Buku Baru

- Method: POST
- Endpoint: `/books`
- Body Request:
  ```json
  {
    "name": "String",
    "year": "Number",
    "author": "String",
    "summary": "String",
    "publisher": "String",
    "pageCount": "Number",
    "readPage": "Number",
    "reading": "Boolean"
  }
  ```

### 2. Mendapatkan Seluruh Buku

- Method: GET
- Endpoint: `/books`
- Query Parameters (opsional):
  - `name`: Filter buku berdasarkan nama
  - `reading`: Filter buku berdasarkan status membaca (0/1)
  - `finished`: Filter buku berdasarkan status selesai (0/1)

### 3. Mendapatkan Detail Buku

- Method: GET
- Endpoint: `/books/{bookId}`

### 4. Mengubah Data Buku

- Method: PUT
- Endpoint: `/books/{bookId}`
- Body Request: (sama dengan menambahkan buku)

### 5. Menghapus Buku

- Method: DELETE
- Endpoint: `/books/{bookId}`

## Pengembangan

Untuk mode pengembangan, gunakan perintah:

```bash
npm run start-dev
```

Ini akan menjalankan server dengan nodemon yang akan memuat ulang server secara otomatis ketika ada perubahan kode.

## Struktur Proyek

```
bookshelf-api/
├── src/
│   ├── handler.js      # Logic handlers
│   ├── routes.js       # Route definitions
│   └── server.js       # Server configuration
├── package.json
└── README.md
```

## Author

[Muhammad Ridho]
