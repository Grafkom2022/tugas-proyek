# Dokumentasi

### Razita Afrina Nuriyan - 2006529360
--------------------------------------

## Cara Menjalankan Program

- Nama file yang harus dibuka di browser: razita.html
- Tombol play: menjalankan animasi default
- Tombol pause: menghentikan animasi default
- Toggle wireframe: mengganti mode dari wireframe ke shading & sebaliknya
- Rod rotation: mengontrol rotasi objek selain orang (dibuat hanya bekerja jika animasi default di-pause)
- Toggle person direction: mengontrol arah jalan objek orang
- Light rotation: merotasi spotlight di arah sumbu terkait

---------------------------

## Proses Pembentukan Objek

**Ketergantungan objek orang:**

- Badan tersambung kepada leher, lengan atas, dan kaki atas.
    
    - Jika badan diputar maka seluruh objek berputar mengikuti badan.

- Leher dan kepala tersambung.

    - Jika leher bergerak maka kepala juga ikut, tetapi tidak sebaliknya.

- Lengan/kaki atas dan lengan/kaki bawah tersambung.

    - Jika lengan/kaki atas bergerak, maka lengan/kaki bawah ikut bergerak.

Struktur node/part:
- Torso
    - Neck
        - Head
    - LeftUpperArm
        - LeftLowerArm
    - RightUpperArm
        - RightLowerArm
    - LeftUpperLeg
        - LeftLowerLeg
    - RightUpperLeg
        - RightLowerLeg

**Ketergantungan objek selain orang:**
- Bagian bawah tersambung bagian atas.
    - Jika bagian bawah bergerak maka seluruh objek mengikuti, tapi tidak sebaliknya.

Struktur node/part:
- LowerRod
    - UpperRod

---------------------------

## Proses Rendering

Rendering dilakukan dengan menyimpan koordinat untuk sebuah cube dan membuat function-function terpisah untuk menggambar setiap node dengan cara memindahkan cube tersebut ke posisi yang sesuai. Jika mode yang dipilih adalah shading, objek digambar menggunakan triangle fan. Wireframe ditunjukkan dengan menggunakan line loop. 

-------------------

## Pembagian Tugas

Razita Afrina Nuriyan (2006529360): Membuat 2 objek berhierarki + animasi & user interaction, setiap lighting, & mode wireframe/shading

------------------

## Referensi

[WebGL2 3D - Directional Lighting](https://webgl2fundamentals.org/webgl/lessons/webgl-3d-lighting-directional.html)

[WebGL2 3D - Point Lighting](https://webgl2fundamentals.org/webgl/lessons/webgl-3d-lighting-point.html)

[WebGL2 3D - Spot Lighting](https://webgl2fundamentals.org/webgl/lessons/webgl-3d-lighting-spot.html)

------------

**Note:** Video demo dapat dilihat pada direktori yang sama dengan file dokumentasi ini, dengan nama demo-razita.mp4.

