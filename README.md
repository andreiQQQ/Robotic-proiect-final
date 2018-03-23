# Robotica-proiect-final
https://drive.google.com/open?id=1PIc0ZvXYDoEzCNCmTHgd-1lGu_auBPBD

Proiectul constă dintr-o platformă care rămâne în echilibru (orizontal) atunci când suportul ei este mișcat

Detalii hardware:
  Am folosit două servo motoare (sevo 9g) pentru a stabili unghiurile în raport cu axele oX și oY. 
  Am folosit un senzor giroscopic (MPU6050) pentru a determina unghiurile dintre suprafața platformei și planul orizontal. 
  Atât platforma propriu-zisă, articuația dintre motoare, cât și suportul au fost printate la imprimanta 3D

Detalii software: 
  Bibliotecile "Wire.h" și "I2Cdev.h" asigură comunicarea între Arduino Uno și senzorul giroscopic. 
  Biblioteca "MPU6050_6Axis_MotionApps20.h" oferă funcțiile necesare pentru calculul unghiurilor față de planul orizontal. 
  Mișcările înregistrate de senzor sunt exprimateinițial sub formă de rotații (unghi) față de o axă (vector din R^3), deci folosind 4 parametri. Poziția relativă față de plan este codificată sub forma unui quaternion (generalizare a numerelor complexe) din care se extrag unghiurile yaw, pitch și roll.
