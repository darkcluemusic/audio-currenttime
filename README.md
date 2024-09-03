# Audio CurrentTime
Berikut merupakan contoh untuk mendapatkan waktu sekarang milidetik untuk memperbarui lirik

## Kode Editor Online
Dari - [CusMeDroid](https://cusmedroid.github.io/live-code-editor/)

## HTML
- Tambahkan di html
```txt
<h1 id="cek"></h1>
<audio id="track" controls>
  <source src="https://firebasestorage.googleapis.com/v0/b/dark-clue.appspot.com/o/post%2Fmemilikimu-kembali%2FMemilikimu%20Kembali.mp3?alt=media&token=bbf16bdf-9397-4e0f-a718-b83e5e222de5" type="audio/mpeg">
</audio>
```

## JAVASCRIPT
- Tambahkan di javascript
```txt
var mCek = document.getElementById('cek');
var audio = document.getElementById('track');
audio.addEventListener('timeupdate',function() {
  var currentTimeMs = audio.currentTime*1000; 
  mCek.innerHTML = Number(currentTimeMs);
  console.log(currentTimeMs); 
}, false); 
```

## Penjelasan
1. Pada h1 memiliki id *cek* berfungsi untuk menampilkan waktu yang berjalan pada saat audio berjalan
2. Pada audio memiliki id *track* sebagai source/src mp3 untuk membuat event atau mendapatkan waktu terbaru
