# Kimlik Doğrulama (Authentication) Modülü Projesine Giriş

## Giriş

Kayıt, oturum açma ve oturum sonlandırma işlevleri sağlayan bir API oluşturmak için "Node.js", "Express" ve "Knex" kullanın.

## Talimatlar

### Görev 1: Proje Kurulumu

Projeyi fokrlayın, klonlayın ve bolca commitleyin.

### Görev 2: MVP

#### 2A - Veritabanı Erişim Fonksiyonları

Erişim fonksiyonlarını `api/users/users-model.js` dosyasına yazacaksınız:

- [x] `bul`
- [x] `goreBul`
- [x] `idyeGoreBul`
- [x] `ekle`

#### 2B - Middleware Fonksiyonları

Auth middlewarelarını `api/auth/auth-middleware.js` dosyasına yazacaksınız:

- [x] `sinirli`
- [x] `usernameBostami`
- [x] `sifreGecerlimi`
- [x] `usernameVarmi`

#### 2C - Uçnoktalar

Kimlik doğrulama, oturumlar ve cookiler kullanılarak izlenecektir. Talimatlar için `api/server.js` a göz atın.

Aşağıdaki uç noktaları yazın. Birincisi `api/users/users-router.js` sayfasında ve diğerleri `api/auth/auth-router.js` sayfasında:

- [ ] `[GET] /api/users`
- [ ] `[POST] /api/auth/register`
- [ ] `[POST] /api/auth/login`
- [ ] `[GET] /api/auth/logout`

#### Users Şeması

`auth.db3` veritabanı, tek bir `users` tablosu içerir:

| bölüm    | veri tipi        | metadata                                      |
| :------- | :--------------- | :-------------------------------------------- |
| user_id  | unsigned integer | primary key, auto-increments, generated by db |
| username | string           | required, unique                              |
| password | string           | required                                      |

#### Notlar

- Testler için `npm test`.
- Proje `migrate`, `rollback` ve `seed` scriptleriyle beraber gelmektedir. veritabanını resetleyebilirsiniz.
- Ek dosyalar oluşturabilirsiniz ancak **mevcut dosyaları veya klasörleri taşımayın veya yeniden adlandırmayın**.
- Fazladan kitaplıklar kurmak veya fazladan betik eklemek dışında `package.json` dosyanızı değiştirmeyin. Mevcut kitaplıkları güncellemeyin.
- Çözümünüzde, en iyi pratikleri izlemeniz ve temiz ve profesyonel sonuçlar üretmeniz çok önemlidir.
- Çalışmanızı gözden geçirmek, iyileştirmek ve değerlendirmek için zaman planlayın.
- Çalışmanızda yazım denetimi ve dilbilgisi denetimi de dahil olmak üzere temel profesyonel cilalama işlemleri gerçekleştirin.

### Görev 3: Esnek Görevler

- Kaydolmak, oturum açmak ve kullanıcı listesini görüntülemek için bir React uygulaması oluşturun. React becerilerinizi geliştirmeye devam etmelisiniz.
