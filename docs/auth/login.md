# Dokumentasi Endpoint OAuth dengan Passport (Google)

## Endpoint 1: Menginisialisasi OAuth dengan Google

### Deskripsi

Endpoint ini digunakan untuk menginisialisasi proses autentikasi OAuth dengan Google.

### Endpoint

`GET /auth/google`

### Code

```javascript
app.get(
    "/auth/google",
    passport.authenticate("google", { scope: ["profile", "email"] })
);
```

## Endpoint 2: Callback Setelah Autentikasi Google

### Deskripsi

Setelah autentikasi berhasil dengan Google, callback ini dijalankan untuk menangani data pengguna yang telah diotentikasi.

### Endpoint

`GET /auth/google/callback`

### Code

```javascript
app.get("auth/google/callback", passport.authenticate("google"), (req, res) => {
    // Setelah autentikasi berhasil, token dapat diambil dari req.user.token
    const accessToken = req.user.accessToken;

    // Lakukan sesuatu dengan token, misalnya, kirimkan kembali ke klien Android
    res.json({ success: true, token: accessToken, user: req.user });
});
```

## Endpoint 3: Penanganan Kegagalan Autentikasi Google

### Deskripsi

Endpoint ini digunakan untuk menangani kasus kegagalan autentikasi dengan Google.

### Endpoint

`GET /auth/google/failure`

### Code

```javascript
app.get("/auth/google/failure", (req, res) => {
    res.status(401).json({
        success: false,
        error: "Google authentication failed.",
    });
});
```

## Endpoint 4: Logout

### Deskripsi

Endpoint ini digunakan untuk logout pengguna dari aplikasi.

### Endpoint

`GET /logout`

### Code

```javascript
app.get("/logout", (req, res) => {
    req.logout((err) => {
        if (err) {
            return res.status(500).json({ error: "Logout failed" });
        }
        return res.status(200).json({ message: "Logout successful" });
    });
});
```

> Dengan dokumentasi ini, pengguna dapat dengan mudah memahami fungsionalitas dan penggunaan masing-masing endpoint dalam autentikasi OAuth dengan Google menggunakan Passport.
