
# نام آزمایش :
تست بازر( بلندگو)

## وسایل مورد نیاز :
* 1 بورد اردینو
* 2 برد بورد
* 3 کابل  USB  برای اتصال بورد اردینو به کامپیوتر
* 4 جامپر
* 5 بلندگو یا بیزر (برای تولید صدا).

## اتصالات 

  *  بلندگو به Arduino:

یک سر بلندگو را به پین دیجیتال 9 (پین speakerPin) متصل کنید.

سر دیگر بلندگو را به GND (زمین) Arduino وصل کنید.

 

  ## شرح آزمایش :

    آغاز کار: در ابتدا، پین بلندگو به عنوان خروجی و پین‌های سوییچ به عنوان ورودی با مقاومت‌های Pull-up تنظیم می‌شوند.

    پخش نت: هر سوییچ مربوط به یک نت از پیانو است و هر بار که سوییچ فشرده می‌شود، نت مربوطه با استفاده از تابع tone() پخش می‌شود.

    خاموش کردن صدا: پس از پخش نت، با استفاده از تابع noTone(), صدا خاموش می‌شود.

  

  ## کد آزمایش :
  #include "pitches.h"

int melody[] =

{  NOTE_C4, NOTE_G3, NOTE_G3, NOTE_GS3, NOTE_G3, 0, NOTE_B3, NOTE_C4};


int noteDurations[] =

{  4, 8, 8, 4, 4, 4, 4, 4};


void setup()

{

  for (int thisNote = 0; thisNote < 8; thisNote++)
  
  {
  
    int noteDuration = 1000 / noteDurations[thisNote];
    
    tone(8, melody[thisNote], noteDuration);
    
    delay(noteDuration + 30);
  
  }
  
}


void loop() {

}  

  

 ## شماتیک مدار:
![توضیح تصویر](https://github.com/Rahel12384/Microprocessor-6/blob/main/micro%203%20/%206666.png)


## خروجی آزمایش:
![alt text](https://github.com/Rahel12384/Microprocessor-6/blob/main/micro%203%20/%20VID_20250107_143723_745%20(1).gif)

  
## نتیجه گیری:
در این آزمایش، توانستیم یک بازر یا بلندگو را تست کنیم
