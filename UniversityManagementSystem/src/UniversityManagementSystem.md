# Üniversite Sınıf Diyagramı

Bu diyagram, üniversite sisteminin sınıflarını ve ilişkilerini tasvir etmektedir.

classDiagram
class Universite {
+ Sınıflik
+ ÇalışmaOfisi
+ Departman
  }

  class Departman {
  + Ofis
  + Çalışan
  }

  class Çalışan {
  ..
  }

  Universite -- Sınıflik
  Universite -- ÇalışmaOfisi
  Universite -- Departman
  Departman -- Ofis
  Departman -- Çalışan


<details>
<summary>University Management System Class Diagram</summary>
    <img src="https://github.com/onur-karakus/OOP/blob/main/UniversityManagementSystem/src/UMS.png" alt="University Management System" title="University Management System" />
</a>
</details>

[<--](../ReadMe.md)
