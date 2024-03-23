Langkah-langkah:
1. Buka terminal atau command prompt Anda dan jalankan perintah berikut untuk membuat proyek Gradle baru
![Screenshot (4)](https://github.com/faizp10/PR16/assets/141897827/c62a2eb2-7285-45ee-9809-f82e9e144bca)

2. Buka file build.gradle di direktori root proyek dan tambahkan kode berikut untuk menentukan tugas khusus

   task greetingTask() {
    doLast {
        String nama = project.hasProperty('nama') ? project.property('nama') : 'Pengguna Gradle'
        println "Halo, $nama! Selamat datang di Dunia Gradle!"
    }
}

4. Anda dapat menjalankan tugas dengan menjalankan perintah <./gradlew greetingTask -Pnama=NamaAnda>
 di terminal
![Screenshot (5)](https://github.com/faizp10/PR16/assets/141897827/9b471c73-6894-45f5-a9e5-c200a290640f)

5. Untuk menambahkan pustaka, Anda dapat menggunakan fitur manajemen dependensi bawaan Gradle. Tambahkan ke file build.gradle Anda kode

   dependencies {

   implementation 'com.google.guava:guava:29.0-jre'

   testImplementation 'junit:junit:4.13'
}

6. Terakhir, dorong proyek ke GitHub dengan membuat repositori baru dan menjalankan perintah berikut

  git init
  
  git add .
  
  git commit -m "Commit awal"
  
  git remote add origin https://github.com/faizp10/PR16.git
  
  git push -u origin master

