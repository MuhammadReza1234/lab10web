<h1 <p align="center"><b>Praktikum 4</b></p></h1> 

**Nama: Muhammad Reza Maulana**

**NIM: 312210303**

**Kelas: TI.22.A3**

---

# Praktikum 10 | PHP OOP

## Langkah langkah praktikum

### 1. Buat file baru dengan nama mobil.php

#### Kode nya seperti dibawah ini :

```php
<?php
/**
* Program sederhana pendefinisian class dan pemanggilan class.
**/
class Mobil
{
    private $warna;
    private $merk;
    private $harga;
    public function __construct()
{
        $this->warna = "Biru";
        $this->merk = "BMW";
        $this->harga = "10000000";
}
    public function gantiWarna ($warnaBaru)
{
        $this->warna = $warnaBaru;
}
public function tampilWarna ()
{
        echo "Warna mobilnya : " . $this->warna;
}
}
// membuat objek mobil
$a = new Mobil();
$b = new Mobil();
// memanggil objek
echo "<b>Mobil pertama</b><br>";
$a->tampilWarna();
echo "<br>Mobil pertama ganti warna<br>";
$a->gantiWarna("Merah");

$a->tampilWarna();
// memanggil objek
echo "<br><b>Mobil kedua</b><br>";
$b->gantiWarna("Hijau");
$b->tampilWarna();
?>
```
- Output :
<img width="883" alt="Cuplikan layar 2023-12-04 101532" src="https://github.com/MuhammadReza1234/lab10web/assets/115516607/06a29f2b-407b-4540-b2db-01d1142d3919">

### 2. Buat file baru dengan nama form.php

#### Kode nya seperti dibawah ini :
---

```php
<?php
/**
* Nama Class: Form
* Deskripsi: CLass untuk membuat form inputan text sederhana
**/
class Form
{
    private $fields = array();
    private $action;
    private $submit = "Submit Form";
    private $jumField = 0;

    public function __construct($action, $submit)
    {
        $this->action = $action;
        $this->submit = $submit;
    }

    public function displayForm()
    {
        echo "<form action='".$this->action."' method='POST'>";
        echo '<table width="100%" border="0">';
        for ($j=0; $j<count($this->fields); $j++) {
            echo "<tr><td
            align='right'>".$this->fields[$j]['label']."</td>";
            echo "<td><input type='text'
            name='".$this->fields[$j]['name']."'></td></tr>";
        }
        echo "<tr><td colspan='2'>";
        echo "<input type='submit' value='".$this->submit."'></td></tr>";
        echo "</table>";
    }

    public function addField($name, $label)
    {
        $this->fields [$this->jumField]['name'] = $name;
        $this->fields [$this->jumField]['label'] = $label;
        $this->jumField ++;
    }
}
?>
```

### 3. Buat file baru dengan nama form_input.php

#### Kode nya seperti dibawah ini
---

```php
<?php
/**
* Program memanfaatkan Program 10.2 untuk membuat form inputan sederhana.
**/
include "form.php";
echo "<html><head><title>Mahasiswa</title></head><body>";
$form = new Form("","Input Form");
$form->addField("txtnim", "Nim");
$form->addField("txtnama", "Nama");
$form->addField("txtalamat", "Alamat");
echo "<h3>Silahkan isi form berikut ini :</h3>";
$form->displayForm();
echo "</body></html>";
?>
```

- Output
<img width="883" alt="Cuplikan layar 2023-12-04 104737" src="https://github.com/MuhammadReza1234/lab10web/assets/115516607/50928233-0cba-4b45-b900-76337b2c3a12">

<h1 <p align="center"><b>======== Sekian Terima Kasih ==========</b></p></h1>
