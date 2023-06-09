# installasi Git
1. Setelah download Git, double click pada file yang di-download. Akan dimunculkan lisensi. Klik Next untuk lanjut.

![01](screenCloud/1.png)

2. Setelah itu, pilih lokasi instalasi. Secara default akan terisi C:\Program Files\Git. Ganti lokasi jika memang anda menginginkan lokasi lain, klik Next

![02](screenCloud/2.png)

3.Pilih komponen. Tidak perlu diubah-ubah, sesuai dengan default saja. Klik pada Next.

![03](screenCloud/3.png)

4.Mengisi shortcut untuk menu Start. Gunakan default (Git), ganti jika ingin mengganti - misalnya Git VCS.

![04](screenCloud/4.png)

5.Pilih editor yang akan digunakan bersama dengan Git. Pada pilihan ini, digunakan VS Code.

![05](screenCloud/5.png)

6.Pada saat instalasi, Git menyediakan akses git melalui Bash maupun command prompt. Pilih pilihan kedua supaya bisa menggunakan dari dua antarmuka tersebut. 
Bash adalah shell di Linux. Dengan menggunakan bash di Windows, pekerjaan di command line Windows bisa dilakukan menggunakan bash - termasuk ekskusi dari Git.

![06](screenCloud/6.png)

7.Pilih OpenSSL untuk HTTPS. Git menggunakan https untuk akes ke repo GitHub atau repo-repo lain (GitLab, Assembla).

![07](screenCloud/7.png)

8.Pilih pilihan pertama untuk konversi akhir baris (CR-LF).

![08](screenCloud/8.png)

9.Pilih PuTTY untuk terminal yang digunakan untuk mengakses Git Bash.

![09](screenCloud/9.png)

10.Untuk opsi ekstra, pilih serta aktifkan 1 dan 2.

![10](screenCloud/10.png)

11.setelah itu proses instalasi akan dilakukan.

![17](screenCloud/17.png)

12.Jika selesai akan muncul dialog pemberitahuan. Klik pada Finish.

![18](screenCloud/18.png)

13.Untuk menjalankan, dari Start menu, ketikkan "Git", akan muncul beberapa pilihan. Pilih "Git Bash" atau "Git GUI".

![19](screenCloud/19.png)

14.Tampilan jika akan menggunakan "Git Bash"

![20](screenCloud/20.png)

15.Tampilan jika akan menggunakan "Git GUI"

![21](screenCloud/21.png)

16.Untuk mencoba dari command prompt, masuk ke command prompt, setelah itu eksekusi "git --version" untuk melihat apakah sudah terinstall atau belum. Jika sudah terinstall dengan benar, makan akan muncul hasil berikut:

![22](screenCloud/22.png)

## Konfigurasi Git
1.Secara minimal, user harus memberitahu Git tentang username serta email yang digunakan setiap kali terjadi perubahan pada repo Git. Username serta email ini yang akan dimasukkan oleh Git ke catatan perubahan di repo. Di sistem operasi Linux atau sejanis (UNIX), konfigurasi ini nantinya akan disimpan di $HOME/.gitconfig. Untuk sistem operasi Windows, konfigurasi ini akan disimpan di C:\Document and Settings\NamaUser dengan nama file .gitconfig. Secara minimal, ada 2 hal yang perlu dikonfigurasi yaitu username dan email. Gunakan perintah berikut:

![1](screenCloud/konfigurasi/1.png)

2.Isian di atas harus disesuaikan dengan nama serta email yang digunakan untuk mendaftar di GitHub. Untuk melihat konfigurasi yang sudah ada:

![2](screenCloud/konfigurasi/2.png)

### Membuat Repo
1.Klik tanda + pada bagian atas setelah login, pilih New repository

![1](screenCloud/Repo/rp1.png)

2.Isikan nama, keterangan, serta lisensi. Jika dikehendaki, bisa membuat repo Private

![2](screenCloud/Repo/rp2.png)

3.Klik Create Repository
Setelah langkah-langkah tersebut, repo akan dibuat dan bisa diakses menggunakan pola https://github.com/username/reponame. Pada repo tersebut, hanya akan muncul 1 file, yaitu LICENSE. Jika memilih membuat README pada saat langkah ke 2, juga akan muncul README.md. Ada atau tidak ada README.md tidak mempunyai efek apapun pada langkah ini.

#### Mengelola Repo

Setelah clone ke komputer lokal, semua manipulasi konten dilakukan di komputer lokal dan hasilnya akan di-push ke remote repo di GitHub. Dengan demikian, jangan berganti-ganti remote lokal, sekali dibuat disitu, tetap berada disitu. Jika kehilangan repo lokal, clone ulang ke direktori yang bersih (kosong) setelah itu baru lakukan pengelolaan repo. Beberapa hal yang biasanya dilakukan akan diuraikan berikut ini.

##### Mengubah Isi - Push Tanpa Branching dan Merging

Perubahan isi bisa terjadi karena satu atau kombinasi beberapa hal berikut:
1.File dihapus
2.File diedit
3,Membuat file / direktori baru
4.Menghapus direktori

Untuk kasus-kasus tersebut, lakukan perubahan di komputer lokal, setelah itu push ke repo.

![1](screenCloud/MengubahIsi/01.png)

![1](screenCloud/MengubahIsi/02.png)

Cara ini lebih mudah tetapi mempunyai resiko jika terjadi kesalahan dalam edit. Cara yang lebih aman tetapi memerlukan langkah yang lebih panjang adalah branching and merging

###### Mengubah Isi dengan Branching and Merging

Dengan menggunakan cara ini, setiap kali akan melakukan perubaham, perubahan itu dilakukan di komputer lokal dengan membuat suatu cabang yang nantinya digunakan untuk menampung perubahan-perubahan tersebut. Setelah itu, cabang itu yang akan dikirim ke repo GitHub untuk dimintai review kemudian digabungkan (merge) ke master. Secara umum, repo yang dibuat biasanya sudah mempunyai satu branch yang disebut dengan master. Cara ini lebih aman, terstruktur, terkendali, dan mempunyai history yang lebih baik. Jika perubahan yang kita buat sudah terlalu kacau dan kita menyesal, maka ada cara untuk "membersihkan" repo lokal kita. Secara umum, langkahnya adalah sebagai berikut:

1.Buat branch untuk menampung perubahan-perubahan

2.Lakukan perubahan-perubahan

3.Add dan commit perubahan-perubahan tersebut ke branch

4.Kembali ke repo master

5.Buat pull request di GitHub

6.Merge pull request di GitHub

7.Merge branch untuk menampung perubahan-perubahan tersebut ke master.

8.Selesai.

![1](screenCloud/MengubahIsi/03.png)

Setelah itu, kirim pull request (PR):

![1](screenCloud/MengubahIsi/05.png)

Setelah membuat PR, PR tersebut bisa di-merge:

![1](screenCloud/MengubahIsi/06.png)

Setelah itu, Confirm Merge, branch yang kita kirimkan tadi sudah dimasukkan ke branch master. Setelah itu, merge di komputer lokal:

![1](screenCloud/MengubahIsi/07.png)

##### Sinkronisasi

Suatu saat, bisa saja terjadi kita menggunakan komputer lain dan mengedit repo melalui repo lokal di komputer lain, setelah itu pindah ke kamputer lain lagi. Saat itu, kita perlu melakukan sinkronisasi ke kemputer lokal. Perintah untuk sinkronisasi adalah:

![1](screenCloud/Singkronisasi/01.png)

###### Membatalkan Perubahan

Praktik yang baik adalah membuat branch pada saat kita akan melakukan perubahan-perubahan. Jika perubahan-perubahan yang kita lakukan sudah sedemikian kacaunya, maka kita bisa membuat supaya perubahan-perubahan yang kacau tersebut hilang dan kembali ke kondisi bersih seperti semula.

![1](screenCloud/MembatalkanPerubahan/001.png)

#### Undo Commit Terakhir
Suatu saat, mungkin kita sudah terlanjur mem-push perubahan ke repo GitHub, setelah itu kita baru menyadari bahwa perubahan tersebut salah. Untuk itu, kita bisa melakukan git revert.

![1](screenCloud/undoCommitTerakhirr/0001.png)

![1](screenCloud/undoCommitTerakhirr/0002.png)

Contoh di atas adalah contoh untuk mengubah README.md dengan beberapa commit. Setelh itu, kita akan mengembalikan ke posisi terakhir sebelum commit terakhir.

Perintah di atas akan membuka editor. Pada editor tersebut kita bisa mengetikkan pesan revert ( = pesan commit untuk pembatalan). Setelah selesai, simpan:

![1](screenCloud/undoCommitTerakhirr/0003.png)

Selanjutnya, tinggal di-push ke repo GitHub.

![1](screenCloud/undoCommitTerakhirr/0004.png)

![1](screenCloud/undoCommitTerakhirr/0005.png)

Jika commit sudah dilakukan, tetapi belum di-push ke repo GitHub (masih berada di lokal), cara membatalkannya:

![1](screenCloud/undoCommitTerakhirr/0006.png)

![1](screenCloud/undoCommitTerakhirr/0007.png)

Untuk kembali ke perubahan pada saat yang sudah lama, yang perlu dilakukan adalah melakukan git revert <posisi> kemudian mengedit secara manual kemudian push ke repo.

![1](screenCloud/undoCommitTerakhirr/0008.png)

Setelah itu, jika dilihat pada file, akan muncul tambahan untuk memudahkan meng-edit. File ini harus di-resolve terlebih dahulu, setelah itu baru di add dan commit:
  
![1](screenCloud/undoCommitTerakhirr/0009.png)
 
Edit file tersebut, setelah itu simpan.

![1](screenCloud/undoCommitTerakhirr/00010.png)
  
Setelah itu, lanjutkan proses revert. Saat git revert --continue isikan pesan revert.
 
![1](screenCloud/undoCommitTerakhirr/00011.png)
  
##### Mengelola Repo Sendiri di Organisasi
Bagian ini merupakan seri tulisan tentang Git. Silahkan ke README.md untuk memahami gambaran garis besar materi-materi yang dituliskan.

Repo yang dibuat bisa diletakkan pada account kita maupun berada pada suatu organisasi. Organisasi bisa kita buat sendiri maupun kita dimasukkan menjadi anggota organisasi. Pada dasarnya, bagian ini sama dengan bagian sebelumnya, hanya saja, pada saat membuat repo Owner dari repo adalah organisasi seperti berikut ini:
 
![1](screenCloud/repoOrganisasi/2.png)

