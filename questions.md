# questions

1 - کدام ویژگی در هر pod در stateful set هویت ثابت داشته باشه؟
نام Pod و DNS ثابت (pod-name + ordinal index) هویت ثابت هر Pod در StatefulSet را تشکیل می‌دهد.

2- در statefulset اگر یک pod حذف شود چه اتفاقی برای نام ان می افتد؟ 
نام Pod تغییر نمی‌کند و با همان نام قبلی دوباره ساخته می‌شود (مثلاً app-0)

3- کدام مورد تفاوت اصلی deployment با statefulset از نظر ذخیره سازی است؟
در StatefulSet از PersistentVolumeClaim اختصاصی برای هر Pod استفاده می‌کند، ولی Deployment معمولاً storage مشترک یا موقت دارد

4- ایجاد pod ها در statefulset چگونه انجام می شود؟
 از Podها در StatefulSet به‌صورت ترتیبی (Ordered) و یکی‌یکی ایجاد می‌شوند.
