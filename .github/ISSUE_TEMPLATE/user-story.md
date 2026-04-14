**As a** client aplikasi e-commerce (frontend atau mikroservis lain)  
**I need** sebuah REST API endpoint untuk membaca detail akun pelanggan berdasarkan ID  
**So that** saya bisa menampilkan atau memproses informasi profil pelanggan tersebut di sistem  
      
### Details and Assumptions
* Endpoint yang akan dikembangkan adalah `GET /accounts/<id>`.
* Mikroservis sudah terhubung dengan database yang berisi data pelanggan (id, nama, email, alamat, dll).
* Respons API harus dikembalikan dalam format JSON.
* Jika ID yang dicari tidak ada di database, sistem harus mengembalikan HTTP Status Code `404 Not Found`.

### Acceptance Criteria     
```gherkin 
Given ada pelanggan yang tersimpan di database dengan ID "123"
When saya mengirimkan HTTP request GET ke endpoint "/accounts/123"
Then saya akan menerima respons dengan status "200 OK" yang berisi data JSON pelanggan tersebut
