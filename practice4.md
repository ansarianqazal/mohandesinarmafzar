
@startuml
left to right direction

skinparam defaultFontName "Arial"
skinparam shadowing false

actor "دانشجو" as Student
actor "مشاور دانشگاه" as Counselor
actor "مدیر سامانه" as Admin

rectangle "سامانه نوبت‌دهی مشاوره دانشگاهی" {
  usecase "ورود به سامانه" as UC1
  usecase "مشاهده زمان‌های آزاد" as UC2
  usecase "رزرو نوبت مشاوره" as UC3
  usecase "مشاهده نوبت‌های من" as UC4
  usecase "لغو نوبت مشاوره" as UC5
  usecase "مدیریت زمان‌های مشاوره" as UC6
  usecase "مشاهده نوبت‌های مشاور" as UC7
  usecase "مدیریت حساب‌های کاربران" as UC8
}

Student --> UC1
Student --> UC2
Student --> UC3
Student --> UC4
Student --> UC5

Counselor --> UC1
Counselor --> UC6
Counselor --> UC7

Admin --> UC1
Admin --> UC8

@enduml
