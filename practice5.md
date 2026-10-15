
@startuml
skinparam defaultFontName "Arial"
skinparam shadowing false

start

:دانشجو وارد سامانه می‌شود;

if (ورود موفق است؟) then (بله)
  :مشاهده زمان‌های آزاد مشاوره;

  if (زمان آزاد وجود دارد؟) then (بله)
    :انتخاب زمان مشاوره;

    if (زمان انتخابی هنوز آزاد است؟) then (بله)
      :ثبت نوبت مشاوره;
      :نمایش پیام تأیید رزرو;
    else (خیر)
      :نمایش پیام پر بودن زمان انتخابی;
    endif

  else (خیر)
    :نمایش پیام نبود زمان آزاد;
  endif

else (خیر)
  :نمایش پیام خطای ورود;
endif

stop
@enduml
