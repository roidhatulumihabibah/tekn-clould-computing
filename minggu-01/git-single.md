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

##### Git untuk Kolaborasi
Bagian ini merupakan seri tulisan tentang Git. Silahkan ke README.md untuk memahami gambaran garis besar materi-materi yang dituliskan.

##### Pendahuluan
Selain untuk mengelola aset digital milik diri sendiri, kita bisa menggunakan Git untuk berkolaborasi dalam suatu repo di GitHub yang bisa diakses bersama. Dalam kasus seperti ini, berarti ada 2 peran:

1.Pemilik repo, sering disebut sebagai upstream author.
  
2.Kontributor, yaitu orang-orang yang akan berkontribusi memberikan konten.

Untuk situasi seperti ini, diasumsikan:
1.Upstream author telah membuat repo git di GitHub
  
2.Kontributor telah mengetahui adanya repo tersebut, tertarik untuk berkontribusi, sudah mengetahui apa yang akan diberikan ke proyek (repo GitHub upstream author) tersebut.
  
3.Pembahasan selanjutnya adalah tentang bagaimana kontributor bisa mengirimkan kontribusi ke repo GitHub milik upstream author.
  
Dalam pembahasan ini:

1.Upstream author adalah oldstager.
  
2.Kontributor adalah bpdp
  
3.Repo dari upstream author adalah playground yang bisa diakses di https://github.com/oldstager/playground
  
###### Fork
Fork adalah membuat clone dari suatu repo di GitHub milik upstream author, diletakkan ke milik kontributor. Fork hanya dilakukan sekali saja. Pada dasarnya, proses untuk fork ini meliputi:

1.Fork repo di web GitHub.
  
2.Clone fork tersebut di komputer lokal.
  
Kontributor harus mem-fork repo upstream author sehingga di repo kontributor muncul repo tersebut. Proses forking ini dijelaskan dengan langkah-langkah berikut:

1.Login ke GitHub
  
2.Akses repo yang akan di-fork: https://github.com/oldstager/playground
  
3.Pada sisi kanan atas, klik Fork:
  
![1](screenCloud/organisasi/1.png)
  
4.Pilih akan ditempatkan di account mana.
  
![1](screenCloud/organisasi/2.png)
  
5.Setelah proses, repo dari upstream author sudah berada di account GitHub kita (kontributor)
  
![1](screenCloud/organisasi/3.png)
  
Setelah proses tersebut, clone di komputer lokal:
  
![1](screenCloud/organisasi/4.png)
  
Setelah itu, konfigurasikan repo lokal kontributor. Pada kondisi saat ini, di komputer lokal sudah terdapat repo playground-1 yang berada pada direktori dengan nama yang sama. Untuk keperluan berkontribusi, ada 2 nama repo yang harus diatur:

1.origin: menunjuk ke repo milik kontributor di GitHub, hasil dari fork.
  
2.upstream: menunjuk ke repo milik upstream author (repo asli) di account 
 oldstager.
 
Repo origin sudah dituliskan konfigurasinya pada saat melakukan proses clone dari repo kontributor. Konfigurasi repo upstream harus dibuat.
  
![1](screenCloud/organisasi/5.png)
 
Tambahkan remote upstream:
  
![1](screenCloud/organisasi/6.png)
  
Hasil:
  
![1](screenCloud/organisasi/6.png)
  
#### Mengirimkan Pull Request
Setiap kali melakukan perubahan, kirim perubahan tersebut. Pengiriman ini disebut dengan Pull Request. Pada posisi ini, kontributor bisa mengirimkan kontribusi dengan cara mengirimkan pull request (PR) ke upstream author. Secara umum, langkah-langkahnya adalah sebagai berikut:

1.Kontributor akan bekerja di repo lokal (create, update, delete isi)
  
2.Commit
  
3.Push ke repo kontributor
  
4.Kirimkan PR ke repo upstream author.
  
5.Upstream author me-review dan kemudian menyetujui (merge) ke master atau menolak PR.
  
6.Jika disetujui dan di-merge ke repo master dari upstream author, sinkronkan repo di komputer lokal dan repo GitHub kontributor.
  
Berikut ini adalah contoh pengiriman perubahan isi README.md dengan menambahkan kontributor.
  
##### Membuat Perubahan di Repo Lokal
Sebelum melakukan perubahan, pastikan:

1.Sudah ada koordinasi secara manual tentang perubahan-perubahan yang akan dilakukan.
  
2.Setelah melakukan perubahan-perubahan, pastikan bahwa isi repo lokal tersinkronisasi dengan repo dari upstream author.
  
3.Cara melakukan sinkronisasi:

![1](screenCloud/caramelakukanSingkronisasi/1.png)
  
4.Lakukan perubahan-perubahan, setelah itu push ke origin (milik kontributor)
  
![1](screenCloud/kontributor/1.png)
  
![1](screenCloud/kontributor/2.png)
  
![1](screenCloud/kontribut/3.png)
  
![1](screenCloud/kontributor/4.png)
  
5.Setelah itu, buka halaman Web dari repo kontributor https://github.com/bpdp/playground-1. Pada halaman tersebut akan ditampilkan isi yang kita push.
  
![1](screenCloud/repokontributor/1.png)
  
6.Pilih Compare and pull request, kemudian isikan deskripsi PR dan klik pada Create pull request:
  
![1](screenCloud/deskripsi/1.png)
  
7.Pada repo upstream author, muncul angka 1 (artinya jumlahnya 1) pada Pull requests di bagian atas.
  
8.Upstream author bisa menyetujui setelah melakukan review: klik pada Pull requests, akan muncul PR dengan message seperti yang ditulis oleh kontributor (Add: contributor). Klik pada PR tersebut, review kemudian klik Merge pull request diikuti dengan Confirm merge. Setelah itu, status akan berubah menjadi Merged.
  
9.Sinkronkan semua repo (lokal maupun GitHub kontributor)

![1](screenCloud/singkronkansemua/1.png)
  
![1](screenCloud/singkronkansemua/2.png)
  
![1](screenCloud/singkronkansemua/3.png)
  
![1](screenCloud/singkronkansemua/4.png)
  
#### Konflik
Ada kemungkinan, jika satu orang mengirimkan PR untuk satu atau lebih file dan sementara itu ada lainnya juga yang mengirimkan PR pada satu atau lebih file yang sama, maka akan terjadi konflik karena ada satu atau lebih file yang sama yang di-edit dan akan di-merge. Jika sampai terjadi kasus seperti ini, maka upatream author harus menolak semua PR dan kemudian masing-masing kontributor diharapkan menyelesaikan secara manual (offline) kemudian memutuskan siapa yang akan mengirimkan PR.
