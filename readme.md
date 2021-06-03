# Vue JS Advance Learning sandbox

Halo semuanya, Vue JS Advance Learning sandbox ini bisa menjadi salah satu alat kalian untuk belajar Vue CLI, Vue Router, Vuex. Silahkan lakukan installasi Vue CLI terlebih dahulu https://cli.vuejs.org/guide/installation.html. 

## Vue CLI & Vue Router

### 1. Project setup

1. git checkout "1.installation"
2. Lakukan project folder setup sesuai dengan nama folder project client-dashboard.
3. Untuk feature yang digunakan pilih Babel, Router, Vuex dan Linter. 
4. Vue yang digunakan versi 2.x, history mode pilih yes, dan pilih Eslint + Airbnb/Standard sebagai confignya, dan jalankan lint on save.
5. Simpan config yang sudah dipilih In dedicated config files
6. Simpan preset yang kalian pilih agar dikemudian hari bisa menggunakan config yang sudah di setting lagi.
7. [referensi](https://cli.vuejs.org/guide/creating-a-project.html#vue-create)

### 2. Registering a new route

1. git checkout "2.register-route"
2. Daftarkan route baru dengan path "/profile" dan route name "Profile" pada file router/index.js, daftarkan Views "Profile.vue" sebagai componentnya. [Ref basic routers](https://router.vuejs.org/guide/#html)
3. Tambahkan router-link baru pada App.vue untuk bisa navigasi ke halaman profile yang baru saja kita buat[Referensi router link](https://router.vuejs.org/api/#router-link)

### 3. Programmatic Navigation

1. git checkout "3.programmatic-navigation"
2. Lakukan navigasi ke halaman dengan path "/login" menggunakan [router push](https://router.vuejs.org/guide/essentials/navigation.html) pada method logout yang terdapat pada komponen Navbar

### 4. Dynamic Route Matching

1. git checkout "4.dynamic-route-matching"
2. Tambahkan route baru dengan path "/users/:id" yang akan merender views UserDetail
3. Manfaatkan programmatic navigation pada method goDetail di component userItem sehinga jika tombol diklik maka kita akan pergi ke halaman UserDetail
4. Lakukan fetch di halaman UserDetail dengan menggunakan axios dan tampilkan datanya kalian bisa melakukan fetch user detail di https://jsonplaceholder.typicode.com/users/:id
5. [Referensi](https://router.vuejs.org/guide/essentials/dynamic-matching.html)

### 5. Nested Route

1. git checkout "5.nested-route"
2. Tambahkan route baru dengan path "profile" pada children route "/users" yang akan merender views UserProfile
3. Tambahkan route baru dengan path "status" pada children route "/users" yang akan merender views UserStatus
4. Tambahkan router-view pada komponen UserDetail
5. [Referensi](https://router.vuejs.org/guide/essentials/nested-routes.html)

### 6. Navigation Guard

1. git checkout "6.nav-guard"
2. Tambahkan beforeRouteEnter yang akan mengecek apakah user memiliki access_token / tidak di localStorage pada Views "Dashboard", jika user tidak memiliki access_token alihkan ke halaman login
5. [Referensi](https://router.vuejs.org/guide/advanced/navigation-guards.html#global-before-guards)

## Vuex

### 7. Vuex State

1. git checkout "7.state"
2. Buatlah data state dengan nama "count" dengan value 0 pada store. [Referensi](https://vuex.vuejs.org/guide/)
3. Ambil data count yang ada di vuex pada component VisitorCount (manfaatkan computed property seperti pada contoh [berikut](https://vuex.vuejs.org/guide/state.html))
4. Tampilkan data count tersebut menggunakan interpolasi

### 8. Mutation (change the state value)

1. git checkout "8.mutation"
2. buatlah mutation dengan nama "incrementCountBy" pada store. Mutation akan menambahkan nilai count pada store sesuai dengan parameter yang dikirim.
3. Panggil mutation incrementCountBy pada method increment di component AddCount, berikan argumen berupa object ```{ ammount: 5 }```ketika pemanggilan mutation.
4. Pastikan ketika button di click maka nilai count pada vuex akan bertambah 5.
5. [Referensi](https://vuex.vuejs.org/guide/mutations.html)
6. Notes: ingat mutation sifatnya synchronous dan berfungsi untuk mengubah state, jadi kalian diperbolehkan untuk memanggil secara langsung mutation pada component jika memang proses perubahan state vuexnya synchronous.

### 9. Action

1. git checkout "9.action"
2. Buatlah action dengan nama "fetchUsers" pada store, lakukan fetching menggunakan axios pada isi "fetchUsers" kalian bisa melakukan fetch ke URL [berikut](https://jsonplaceholder.typicode.com/users)
3. Buatlah mutation dengan nama "SET_USERS" pada store yang berfungsi untuk merubah state users sesuai dengan payload yang dikirim.
4. Panggil mutation SET_USERS ketika berhasil mendapatkan data users di action fetchUsers.
5. Panggil action fetchUsers pada component UserList di lifecycle "created".
6. [Referensi](https://vuex.vuejs.org/guide/actions.html)
7. Notes:
   - Dalam action kalian bisa melakukan proses async seperti melakukan fetch ke DB dan sebagainya
   - Pada action kita dilarang untuk melakukan perubahan state secara langsung, kita diwajibkan melakukan perubahan state melalui mutation
