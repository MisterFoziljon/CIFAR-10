## CIFAR-10 dataseti yordamida obyektlarni qaysi turkumga tegishli ekanligini bashorat qilish

#### 1. ```CIFAR-10``` dataseti haqida qisqacha ma'lumot
```CIFAR-10``` (Kanada Ilg'or Tadqiqotlar Instituti) ma'lumotlar to'plami odatda Machine Learning va Computer Vision algoritmlarini o'rgatish uchun ishlatiladigan va  tadqiqotlar uchun eng koʻp foydalaniladigan maʼlumotlar toʻplamidir. ```CIFAR-10``` ma'lumotlar to'plami 10 ta turli sinflardan iborat bo'lib, 60 000 ta 32x32 rangli tasvirlarni o'z ichiga oladi. 10 ta sinf: ```samolyot```, ```avtomobil```, ```qush```, ```mushuk```, ```kiyik```, ```it```, ```qurbaqa```, ```ot```, ```kema``` va ```yuk mashina```larini ifodalaydi. Har bir sinfning 6000 ta tasviri mavjud.

![cmd](https://github.com/MisterFoziljon/CIFAR-10/blob/main/rasmlar/cifar10.jpg)

#### 2. Loyihani yuklab olish uchun quyidagi ketma-ketlikni bajaring:
  * `windows+R` klavishlarini bosing va paydo bo'lgan oynaga `cmd` buyrug'ini yozing OK tugmachasini bosing.
  
  ![cmd](https://github.com/MisterFoziljon/CIFAR-10/blob/main/rasmlar/cmd.png)

  * Loyihani quyidagi link yordamida yuklab oling. (Loyiha uchun yaratilgan fayl adresni o'zingiz ko'rsatishingiz mumkin)

        C:\> git clone https://github.com/MisterFoziljon/CIFAR-10.git

  * Loyiha joylashgan faylga kiring.
         
        C:\> cd CIFAR-10


#### 3. Proyektni ishlatish uchun kerakli modullarni virtual environment yaratib o'rnatib oling.
* O'zingizdagi pip ni so'nggi versiyasiga yangilang.

        C:\CIFAR-10> python -m pip install --upgrade pip
        
* virtual environment yaratish uchun virtualenv modulini o'rnating.
        
        C:\CIFAR-10> python -m pip install --user virtualenv

* Yangi environment yaratish uchun unga nom bering.
        
        C:\CIFAR-10> python -m venv sizning_env
        
* Virtual environmentni ishga tushiring(aktivlashtiring).
        
        C:\CIFAR-10> sizning_env\Scripts\activate.bat
        
* Virtual environment ichiga loyiha ishlashi uchun kerakli bo'lgan modullarni o'rnating (requirements.txt faylining ichida barchasi mavjud).
        
        (sizning_env) C:\CIFAR-10> pip install -r requirements.txt


#### 4. Proyektni ishlatish uchun jupyter notebook ni ishga tushiring.

        (sizning_env) C:\CIFAR-10> jupyter notebook
        
  * ```CNN yordamida model o'qitish.ipynb``` ni ishga tushiring. Usbu notebookda Keras.io saytidagi MNIST datasetini o'qib olish, uni train va test datalariga ajratish, datalarni size va shape larini train uchun moslash hamda normallashtirish ko'rsatilgan. Dataset yordamida Convolutional Neural Network ishlab chiqilgan va u yordamida model train va evaluate qilingan. Model h5 formatda saqlanadi. Ushbu notebookni birinchi bo'lib ishga tushirib ```modelni qayta o'qiting```!!! Chunki model githubga yuklanmadi.
  
![streamlit1](https://github.com/MisterFoziljon/CIFAR-10/blob/main/rasmlar/graphic.png)
  
  * ```Modelni sinovdan o'tkazish.ipynb``` ni ishga tushiring. Ushbu notebook yordamida saqlangan modelni load qilish va yangi test qilish datalari yordamida bashorat qilish (predict) ko'rsatib o'tilgan.


#### 4. Proyektni streamlit yordamida deploy qilish.

        (sizning_env) C:\CIFAR-10> streamlit run streamlit.py

  * Proyekt ```local server```da ishga tushadi va quyidagicha ko'rinishda bo'ladi:


![streamlit1](https://github.com/MisterFoziljon/CIFAR-10/blob/main/rasmlar/streamlit1.png)
  
  * Rasm faylini yuklab oling va ```Predict``` tugmachasini bosing. Model yuklab olingan tasvirni qaysi turkumga tegishli ekanligini bashorat qiladi. Bundan tashqari softmaxdan chiqqan ehtimollik natijasi ham ekranga chiqadi.


![streamlit3](https://github.com/MisterFoziljon/CIFAR-10/blob/main/rasmlar/streamlit2.png)
