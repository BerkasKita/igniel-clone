# Memasang Informasi Tema

<p align="center">
  <img src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgNTCzHTCD85E9HayKrkWp1dO-B7je83mZKPO2Pck_g3pznJFBxjFLSKMI_W1Jf2NHKDLt_1HUtSJ-BMXiLvnxjxh4iEzhxKMYPMg-uu0oWmgQngUPzMujsHKtIOhTZzWawckzS1HqpETrCNI6B1RE63qiwvVEpOtOHhRfY2wfPN5Dh8u7uvVaHSNCCdiY/s0/Screenshot%202025-05-18%20163004.png" alt="Memasang Informasi Tema">
</p>

cari kode ini
```xml
<b:widget cond='data:view.isPost and !data:view.isPreview' id='HTML03' locked='true' title='Trending Serupa' type='HTML' version='2' visible='true'>...</b:widget>
```

dan letakkan dibawahnya kode ini

```xml
<b:widget cond='data:view.url == data:blog.homepageUrl path &quot;/2025/05/test-template.html&quot;' id='HTML1' locked='false' title='Informasi Tema' type='HTML' visible='true'>
  <b:widget-settings>
    <b:widget-setting name='content'><![CDATA[...]]></b:widget-setting>
  </b:widget-settings>
  <b:includable id='main'>
    <b:if cond='!data:blog.isMobileRequest'>
      <b:include name='widget-title'/>
      <div class='widget-content'>
        <data:content/>
      </div>
    </b:if>
  </b:includable>
</b:widget>
```

pada `id='HTML1'` ganti dengan id yang belum tersedia, contoh `id='HTML100'` atau `id='HTML101'` dan seterusnya (Setiap Widget tidak boleh memiliki id yang sama).

pada `<![CDATA[...]]>` ganti dengan tag html ini 

```html
<div class="card-atas">
  <a class="tema-demo btn-outline f" href="https://igniplex.blogspot.com" rel="noopener" target="_blank" title="Demo Igniplex">
    <svg class="fill" viewbox="0 0 24 24">
      <path d="M12,9A3,3 0 0,1 15,12A3,3 0 0,1 12,15A3,3 0 0,1 9,12A3,3 0 0,1 12,9M12,4.5C17,4.5 21.27,7.61 23,12C21.27,16.39 17,19.5 12,19.5C7,19.5 2.73,16.39 1,12C2.73,7.61 7,4.5 12,4.5M3.18,12C4.83,15.36 8.24,17.5 12,17.5C15.76,17.5 19.17,15.36 20.82,12C19.17,8.64 15.76,6.5 12,6.5C8.24,6.5 4.83,8.64 3.18,12Z" fill="%2377828d"></path>
    </svg>
    Live Preview (Demo)
  </a>
</div>
<div class="card-isi">
  <div class="card-judul b f">
    <div class="card-tipe">
      PREMIUM
    </div>
    <div class="card-harga aksen">
      <sup>Rp</sup>230.000
      <span class="usd">/ <sup>$</sup>28</span>
    </div>
  </div>
  <div class="card-info">
    <div class="f">
      <span>Nama</span>
      Igniplex
    </div>
    <div class="f">
      <span>Versi Terbaru</span>
      v3
    </div>
    <div class="f">
      <span>Tanggal Rilis</span>
      27 Februari 2023
    </div>
    <div class="f">
      <span>Pembaruan Terakhir</span>
      27 Februari 2024
    </div>
  </div>
  <div class="card-terms kecil">
    <ul>
      <li class="f">
        <svg class="yes" viewbox="0 0 24 24">
          <path d="M12 22C17.5 22 22 17.5 22 12C22 6.5 17.5 2 12 2C6.5 2 2 6.5 2 12C2 17.5 6.5 22 12 22Z"></path>
          <path d="M7.75 12L10.58 14.83L16.25 9.17004"></path>
        </svg>
        <span><strong>WAJIB</strong> membaca <label class="aksen pointer" for="sk"><u>syarat dan ketentuan</u></label> yang berlaku sebelum membeli.</span>
      </li>
      <li class="f">
        <svg class="yes" viewbox="0 0 24 24">
          <path d="M12 22C17.5 22 22 17.5 22 12C22 6.5 17.5 2 12 2C6.5 2 2 6.5 2 12C2 17.5 6.5 22 12 22Z"></path>
          <path d="M7.75 12L10.58 14.83L16.25 9.17004"></path>
        </svg>
        <span>Unlimited domain dengan syarat pemiliknya harus satu orang yang sama.</span>
      </li>
      <li class="f">
        <svg class="no" viewbox="0 0 24 24">
          <path d="M12 22C17.5 22 22 17.5 22 12C22 6.5 17.5 2 12 2C6.5 2 2 6.5 2 12C2 17.5 6.5 22 12 22Z"></path>
          <path d="M9.16998 14.83L14.83 9.17004"></path>
          <path d="M14.83 14.83L9.16998 9.17004"></path>
        </svg>
        <span>Tidak boleh dibagikan / dijual ulang.</span>
      </li>
    </ul>
  </div>
  <div class="card-unduh">
    <label for="beli">
      <div class="tema-beli btn-aksen flex-grow pointer f" title="Beli">
        <svg class="fill" viewbox="0 0 24 24">
          <path d="M17,18A2,2 0 0,1 19,20A2,2 0 0,1 17,22C15.89,22 15,21.1 15,20C15,18.89 15.89,18 17,18M1,2H4.27L5.21,4H20A1,1 0 0,1 21,5C21,5.17 20.95,5.34 20.88,5.5L17.3,11.97C16.96,12.58 16.3,13 15.55,13H8.1L7.2,14.63L7.17,14.75A0.25,0.25 0 0,0 7.42,15H19V17H7C5.89,17 5,16.1 5,15C5,14.65 5.09,14.32 5.24,14.04L6.6,11.59L3,4H1V2M7,18A2,2 0 0,1 9,20A2,2 0 0,1 7,22C5.89,22 5,21.1 5,20C5,18.89 5.89,18 7,18M16,11L18.78,6H6.14L8.5,11H16Z"></path>
        </svg>
        Beli
      </div>
    </label>
  </div>
  <div class="card-bantu">
    <a class="aksen" href="/p/help.html" rel="noopener" target="_blank" title="Bantuan">
      <svg viewbox="0 0 24 24">
        <path d="M4 13m0 2a2 2 0 0 1 2 -2h1a2 2 0 0 1 2 2v3a2 2 0 0 1 -2 2h-1a2 2 0 0 1 -2 -2z"></path>
        <path d="M15 13m0 2a2 2 0 0 1 2 -2h1a2 2 0 0 1 2 2v3a2 2 0 0 1 -2 2h-1a2 2 0 0 1 -2 -2z"></path>
        <path d="M4 15v-3a8 8 0 0 1 16 0v3"></path>
      </svg>
      Bantuan (Help)
    </a>
  </div>
</div>
```
dan hasilnya akan seperti ini 

```xml
<![CDATA[<div class="card-atas">
  <a class="tema-demo btn-outline f" href="https://igniplex.blogspot.com" rel="noopener" target="_blank" title="Demo Igniplex">
    <svg class="fill" viewbox="0 0 24 24">
      <path d="M12,9A3,3 0 0,1 15,12A3,3 0 0,1 12,15A3,3 0 0,1 9,12A3,3 0 0,1 12,9M12,4.5C17,4.5 21.27,7.61 23,12C21.27,16.39 17,19.5 12,19.5C7,19.5 2.73,16.39 1,12C2.73,7.61 7,4.5 12,4.5M3.18,12C4.83,15.36 8.24,17.5 12,17.5C15.76,17.5 19.17,15.36 20.82,12C19.17,8.64 15.76,6.5 12,6.5C8.24,6.5 4.83,8.64 3.18,12Z" fill="%2377828d"></path>
    </svg>
    Live Preview (Demo)
  </a>
</div>
<div class="card-isi">
  <div class="card-judul b f">
    <div class="card-tipe">
      PREMIUM
    </div>
    <div class="card-harga aksen">
      <sup>Rp</sup>230.000
      <span class="usd">/ <sup>$</sup>28</span>
    </div>
  </div>
  <div class="card-info">
    <div class="f">
      <span>Nama</span>
      Igniplex
    </div>
    <div class="f">
      <span>Versi Terbaru</span>
      v3
    </div>
    <div class="f">
      <span>Tanggal Rilis</span>
      27 Februari 2023
    </div>
    <div class="f">
      <span>Pembaruan Terakhir</span>
      27 Februari 2024
    </div>
  </div>
  <div class="card-terms kecil">
    <ul>
      <li class="f">
        <svg class="yes" viewbox="0 0 24 24">
          <path d="M12 22C17.5 22 22 17.5 22 12C22 6.5 17.5 2 12 2C6.5 2 2 6.5 2 12C2 17.5 6.5 22 12 22Z"></path>
          <path d="M7.75 12L10.58 14.83L16.25 9.17004"></path>
        </svg>
        <span><strong>WAJIB</strong> membaca <label class="aksen pointer" for="sk"><u>syarat dan ketentuan</u></label> yang berlaku sebelum membeli.</span>
      </li>
      <li class="f">
        <svg class="yes" viewbox="0 0 24 24">
          <path d="M12 22C17.5 22 22 17.5 22 12C22 6.5 17.5 2 12 2C6.5 2 2 6.5 2 12C2 17.5 6.5 22 12 22Z"></path>
          <path d="M7.75 12L10.58 14.83L16.25 9.17004"></path>
        </svg>
        <span>Unlimited domain dengan syarat pemiliknya harus satu orang yang sama.</span>
      </li>
      <li class="f">
        <svg class="no" viewbox="0 0 24 24">
          <path d="M12 22C17.5 22 22 17.5 22 12C22 6.5 17.5 2 12 2C6.5 2 2 6.5 2 12C2 17.5 6.5 22 12 22Z"></path>
          <path d="M9.16998 14.83L14.83 9.17004"></path>
          <path d="M14.83 14.83L9.16998 9.17004"></path>
        </svg>
        <span>Tidak boleh dibagikan / dijual ulang.</span>
      </li>
    </ul>
  </div>
  <div class="card-unduh">
    <label for="beli">
      <div class="tema-beli btn-aksen flex-grow pointer f" title="Beli">
        <svg class="fill" viewbox="0 0 24 24">
          <path d="M17,18A2,2 0 0,1 19,20A2,2 0 0,1 17,22C15.89,22 15,21.1 15,20C15,18.89 15.89,18 17,18M1,2H4.27L5.21,4H20A1,1 0 0,1 21,5C21,5.17 20.95,5.34 20.88,5.5L17.3,11.97C16.96,12.58 16.3,13 15.55,13H8.1L7.2,14.63L7.17,14.75A0.25,0.25 0 0,0 7.42,15H19V17H7C5.89,17 5,16.1 5,15C5,14.65 5.09,14.32 5.24,14.04L6.6,11.59L3,4H1V2M7,18A2,2 0 0,1 9,20A2,2 0 0,1 7,22C5.89,22 5,21.1 5,20C5,18.89 5.89,18 7,18M16,11L18.78,6H6.14L8.5,11H16Z"></path>
        </svg>
        Beli
      </div>
    </label>
  </div>
  <div class="card-bantu">
    <a class="aksen" href="/p/help.html" rel="noopener" target="_blank" title="Bantuan">
      <svg viewbox="0 0 24 24">
        <path d="M4 13m0 2a2 2 0 0 1 2 -2h1a2 2 0 0 1 2 2v3a2 2 0 0 1 -2 2h-1a2 2 0 0 1 -2 -2z"></path>
        <path d="M15 13m0 2a2 2 0 0 1 2 -2h1a2 2 0 0 1 2 2v3a2 2 0 0 1 -2 2h-1a2 2 0 0 1 -2 -2z"></path>
        <path d="M4 15v-3a8 8 0 0 1 16 0v3"></path>
      </svg>
      Bantuan (Help)
    </a>
  </div>
</div>]]>
```

Terakhir pada `cond='data:view.url == data:blog.homepageUrl path &quot;/2025/05/test-template.html&quot;'` 

bagian `/2025/05/test-template.html` bisa seuaikan dengan url blog kamu. 

contoh: `https://www.yoredaze.com/2025/05/test-template.html` menjadi `/2025/05/test-template.html`

# Memasang Url Demo pada mode mobile

<p align="center">
  <img src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEirpjamXeFBIwxtqdtB4uj3I0eyNpIlyHlVy5FPfNaAGkV3R9lMaQWV118DOUT1M7urPKreBJCgnXpoP1rUS-sg4k9ZvwAKeyO1VZLfnWrbM1_l423EMf-meSTc87wDx-Er_pw91-E_MaKw1-vBjOofJOkHfwyQ6_xK1r15mIy6XR3V-5NGzPcBYIknfIM/s0/Screenshot%202025-05-18%20223530.png" alt="Memasang Url Demo pada mode mobile">
</p>
