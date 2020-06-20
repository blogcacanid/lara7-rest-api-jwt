# lara7-rest-api-jwt
Rest API Dengan JSON Web Token Laravel 7

> https://blog.cacan.id/rest-api-dengan-json-web-token-laravel-7

![000](https://user-images.githubusercontent.com/51890752/84871174-64c85180-b0aa-11ea-881a-4c7cc86e6576.jpg)


# Cara Penggunaan:

## Clone dari GitHub:
git clone https://github.com/blogcacanid/lara7-rest-api-jwt.git

## Lalu masuk ke direktori project:
cd lara7-rest-api-jwt

## Selanjutnya jalankan perintah berikut secara berurutan:
- composer install
- cp .env.example .env
- php artisan key:generate
- php artisan jwt:secret
- php artisan migrate

## Testing
Jalankan Laravel 7 dengan menggunakan perintah berikut:
- php artisan serve

Lalu buka browser dan ketikkan URL http://localhost:8000

### Testing via Postman
Selanjutnya kita akan testing menggunakan Postman.

#### Register
Pertama-tama kita daftarkan user baru terlebih dahulu agar kita bisa melakukan login.
Buka postman lalu pilih method POST kemudian ketikkkan URL http://localhost:8000/api/register
Kemudian pilih tab Body. Lalu pada radiobox pilih raw dan typenya pilih JSON. Selanjutnya pada bagian textbox inputkan data registrasinya seperti berikut:
{
"name": "Rony",
"email": "rony@rony.com",
"password": "qwertyui",
"password_confirmation": "qwertyui"
}
Selanjutnya klik tombol Send

![001](https://user-images.githubusercontent.com/51890752/85212774-72b6f480-b380-11ea-83a5-f515b5612b12.jpg)


#### Login
Setelah registrasi berhasil selanjutnya kita coba untuk login dengan user yang sudah kita registrasikan tersebut.
Buka postman lalu pilih method POST kemudian ketikkkan URL http://localhost:8000/api/login
Kemudian pilih tab Body. Lalu pada radiobox pilih raw raw dan typenya pilih JSON. Selanjutnya pada bagian textbox inputkan data email dan password untuk login:
{
"email": "rony@rony.com",
"password": "qwertyui"
}
Selanjutnya klik tombol Send

![002](https://user-images.githubusercontent.com/51890752/85212788-882c1e80-b380-11ea-8a03-3c6db261ebb0.jpg)

Jika login berhasil, maka kita akan mendapatkan access token. Access Token tersebut nanti akan kita gunakan untuk proses selanjutnya. 

##### Profile
Selanjutnya kita akan mencoba mengakses link Profile.
Link profile ini hanya bisa diakses dengan menggunakan token.
Buka postman lalu pilih method GET kemudian ketikkkan URL http://localhost:8000/api/profile
Kemudian pilih tab Authorization. Lalu pada combo TYPE pilih Bearear Token. Selanjutnya pada textbox Token isi dengan data access token yang didapat pada saat login sebelumnya.
Selanjutnya klik tombol Send
![003](https://user-images.githubusercontent.com/51890752/85212799-9e39df00-b380-11ea-9d06-5ecb3cc214c3.jpg)


<p align="center"><img src="https://res.cloudinary.com/dtfbvvkyp/image/upload/v1566331377/laravel-logolockup-cmyk-red.svg" width="400"></p>

<p align="center">
<a href="https://travis-ci.org/laravel/framework"><img src="https://travis-ci.org/laravel/framework.svg" alt="Build Status"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://poser.pugx.org/laravel/framework/d/total.svg" alt="Total Downloads"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://poser.pugx.org/laravel/framework/v/stable.svg" alt="Latest Stable Version"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://poser.pugx.org/laravel/framework/license.svg" alt="License"></a>
</p>

## About Laravel

Laravel is a web application framework with expressive, elegant syntax. We believe development must be an enjoyable and creative experience to be truly fulfilling. Laravel takes the pain out of development by easing common tasks used in many web projects, such as:

- [Simple, fast routing engine](https://laravel.com/docs/routing).
- [Powerful dependency injection container](https://laravel.com/docs/container).
- Multiple back-ends for [session](https://laravel.com/docs/session) and [cache](https://laravel.com/docs/cache) storage.
- Expressive, intuitive [database ORM](https://laravel.com/docs/eloquent).
- Database agnostic [schema migrations](https://laravel.com/docs/migrations).
- [Robust background job processing](https://laravel.com/docs/queues).
- [Real-time event broadcasting](https://laravel.com/docs/broadcasting).

Laravel is accessible, powerful, and provides tools required for large, robust applications.

## Learning Laravel

Laravel has the most extensive and thorough [documentation](https://laravel.com/docs) and video tutorial library of all modern web application frameworks, making it a breeze to get started with the framework.

If you don't feel like reading, [Laracasts](https://laracasts.com) can help. Laracasts contains over 1500 video tutorials on a range of topics including Laravel, modern PHP, unit testing, and JavaScript. Boost your skills by digging into our comprehensive video library.

## Laravel Sponsors

We would like to extend our thanks to the following sponsors for funding Laravel development. If you are interested in becoming a sponsor, please visit the Laravel [Patreon page](https://patreon.com/taylorotwell).

- **[Vehikl](https://vehikl.com/)**
- **[Tighten Co.](https://tighten.co)**
- **[Kirschbaum Development Group](https://kirschbaumdevelopment.com)**
- **[64 Robots](https://64robots.com)**
- **[Cubet Techno Labs](https://cubettech.com)**
- **[Cyber-Duck](https://cyber-duck.co.uk)**
- **[Many](https://www.many.co.uk)**
- **[Webdock, Fast VPS Hosting](https://www.webdock.io/en)**
- **[DevSquad](https://devsquad.com)**
- [UserInsights](https://userinsights.com)
- [Fragrantica](https://www.fragrantica.com)
- [SOFTonSOFA](https://softonsofa.com/)
- [User10](https://user10.com)
- [Soumettre.fr](https://soumettre.fr/)
- [CodeBrisk](https://codebrisk.com)
- [1Forge](https://1forge.com)
- [TECPRESSO](https://tecpresso.co.jp/)
- [Runtime Converter](http://runtimeconverter.com/)
- [WebL'Agence](https://weblagence.com/)
- [Invoice Ninja](https://www.invoiceninja.com)
- [iMi digital](https://www.imi-digital.de/)
- [Earthlink](https://www.earthlink.ro/)
- [Steadfast Collective](https://steadfastcollective.com/)
- [We Are The Robots Inc.](https://watr.mx/)
- [Understand.io](https://www.understand.io/)
- [Abdel Elrafa](https://abdelelrafa.com)
- [Hyper Host](https://hyper.host)
- [Appoly](https://www.appoly.co.uk)
- [OP.GG](https://op.gg)
- [云软科技](http://www.yunruan.ltd/)

## Contributing

Thank you for considering contributing to the Laravel framework! The contribution guide can be found in the [Laravel documentation](https://laravel.com/docs/contributions).

## Code of Conduct

In order to ensure that the Laravel community is welcoming to all, please review and abide by the [Code of Conduct](https://laravel.com/docs/contributions#code-of-conduct).

## Security Vulnerabilities

If you discover a security vulnerability within Laravel, please send an e-mail to Taylor Otwell via [taylor@laravel.com](mailto:taylor@laravel.com). All security vulnerabilities will be promptly addressed.

## License

The Laravel framework is open-sourced software licensed under the [MIT license](https://opensource.org/licenses/MIT).
