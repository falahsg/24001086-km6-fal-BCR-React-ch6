# Binar Car Rental - React Challenge CH 06

Membuatlah aplikasi Binar Car Rental dengan menggunakan React. Aplikasi dibuat berdasarkan [desain dari figma](https://www.figma.com/file/PKNYfwTP0UvhDV51msj2oK/BCR---Binar-Car-Rental%3A-Challenge-4?type=design&node-id=111-5698&mode=design).

# Frontend Server
## Setup Server

    cd frontend
    npm install
    
`npm install` diperlukan untuk menginstall semua dependencies yang diperlukan dalam project.  

## Running Server

    cd frontend
    npm run dev

Server frontend secara default akan berjalan di Vite http://localhost:5173/

## Server Routing
| Page | Route | Default Route |
|--|--|--|
| Homepage | `/` | http://localhost:5173/ |
| Page Search | `/cars` | http://localhost:5173/cars |
 
 

# Backend Server
## Setup Server

    cd backend
    npm install
    
`npm install` diperlukan untuk menginstall semua dependencies yang diperlukan dalam project.

Lalu buat file .env dan mengisinya sesuai dengan .env.example (PASTIKAN PORT TETAP DI 3000) bila tidak ingin mengubah settingan axios di front end
bila diubah port selain 3000 pada backend, maka sesuaikan port pada frontend yang berada di `frontend/src/components/cars/FilterCarData/index.js`
    
Setelah itu pastikan [PostgreSQL](https://www.postgresql.org/download/) sudah ter-install dan berjalan di komputer. Kemudian setup file `backend/config/database.js` sesuai dengan settings database PostgreSQL yang sedang berjalan. Lanjut jalankan perintah berikut di terminal.

    cd backend
    sequelize db:create
    sequelize db:migrate
    
    // OPTIONAL: untuk menambahkan dummy data ke DB
    sequelize db:seed:all
    sequelize db:seed:undo // Untuk menghapus dummy data

## Running Server

    cd backend
    npm run dev

Server frontend secara default akan berjalan di `http://localhost:3000/`  
Port server bisa diganti di dalam file `backend/config/database.js`   

## REST API Endpoints
### Hello World Test

Test untuk memastikan REST API telah berjalan dengan baik.

#### *HTTP Request*
> **GET**   
> `/api/v1`

#### *Default Request URL*

    http://localhost:3000/api/v1