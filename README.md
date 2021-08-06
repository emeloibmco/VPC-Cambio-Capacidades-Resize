# VPC - Cambiar Tamaño (Resize) ☁⚙
Los servidores virtuales se configuran mediante perfiles o una combinación de atributos de instancia, como la cantidad de CPU virtuales, la cantidad de RAM, el ancho de banda de la red y más, que definen el tamaño y las capacidades de la instancia del servidor virtual. Cuando implementa una *VSI* en *IBM Cloud*, puede cambiar el tamaño de su instancia de servidor virtual y escalar verticalmente a cualquier tamaño de perfil admitido en minutos. Puede aumentar o disminuir la cantidad de vCPU y RAM disponibles para una mayor flexibilidad en la administración de la carga de trabajo para abordar los cambios en los requisitos de recursos, optimizar el costo o el rendimiento de la carga de trabajo.

La presente guía se centra en mostrar los pasos que se deben realizar para duplicar y reducir a la mitad la cantidad de vCPU y memoria de una *VSI* en *VPC*.

## Índice  📰
1. [Pre-Requisitos](#Pre-Requisitos-pencil)
2. [Detener VSI](#Detener-VSI-stop_sign)
3. [Cambiar tamaño de VSI duplicando vCPU y memoria](#Cambiar-tamaño-de-VSI-duplicando-vCPU-y-memoria-outbox_tray-computer)
4. [Cambiar tamaño de VSI reduciendo vCPU y memoria a la mitad](#Cambiar-tamaño-de-VSI-reduciendo-vCPU-y-memoria-a-la-mitad-inbox_tray-computer)
7. [Referencias](#Referencias-mag)
8. [Autores](#Autores-black_nib)
<br />

## Pre-Requisitos :pencil:
* Contar con una cuenta en <a href="https://cloud.ibm.com/"> IBM Cloud</a>.
* Contar con una *VPC* y una *VSI*.
<br />

## Detener VSI :stop_sign:
El primer paso que se debe realizar antes de aplicar cambios de tamaño a los perfiles de la *VSI*, es detenerla. Para ello, ingrese a ```Infrestructura VPC``` ➡ ```Computación``` ➡ ```Instancias de servidor virtual``` y visualice la *VSI* sobre la que desea aplicar cambios. De click en los tres puntos y seleccione la opción ```Detener```. Luego de esto espere unos minutos mientras la *VSI* se detiene y recargue la página.  
<br />

<p align="center"><img width="700" src="https://github.com/emeloibmco/VPC-Cambio-Capacidades-Resize/blob/main/Im%C3%A1genes/Detener%20VSI.gif"></p>
<br />

## Cambiar tamaño de VSI duplicando vCPU y memoria :outbox_tray: :computer:
Para cambiar el tamaño de la *VSI* duplicando la cantidad de los vCPU y memoria, siga los pasos que se muestran a continuación:
<br />

1. Visualiza la *VSI* que se encuentra en estado ```detenido```, de click en los 3 puntos y seleccione la opción ```Cambiar tamaño```.
<br />

2. Cuando aparezca la nueva ventana, cambie el perfil de su *VSI*. Para este caso, se cuenta con una *VSI* de perfil ```bx2-2x8``` que se cambia a ```bx2-4x16```.
<br />

3. Después de cambiar el perfil, acepte los cambios en el importe de pago y de click en el botón ```Redimensionar instancia de servidor virtual```.
<br />

4. Espere mientras aparece la nueva configuración y en los tres puntos de click en la opción ```Iniciar``` para poner nuevamente en ejecución la *VSI*.
<br />

<p align="center"><img width="700" src="https://github.com/emeloibmco/VPC-Cambio-Capacidades-Resize/blob/main/Im%C3%A1genes/Duplicar%20Tama%C3%B1o.gif"></p>
<br />

Cuando la *VSI* esté lista deberá observar el estado ```En ejecución```.
<br />

<p align="center"><img width="700" src="https://github.com/emeloibmco/VPC-Cambio-Capacidades-Resize/blob/main/Im%C3%A1genes/DuplicarOK.PNG"></p>
<br />

## Cambiar tamaño de VSI reduciendo vCPU y memoria a la mitad :inbox_tray: :computer:
Para cambiar el tamaño de la *VSI* reduciendo la cantidad de los cCPU y memoria, recuerde detener la instancia como se indicó en el paso [Detener VSI](#Detener-VSI-stop_sign). Posteriormente, siga los pasos que se muestran a continuación:
<br />

1. Visualiza la *VSI* que se encuentra en estado ```detenido```, de click en los 3 puntos y seleccione la opción ```Cambiar tamaño```.
<br />

2. Cuando aparezca la nueva ventana, cambie el perfil de su *VSI*. Para este caso, se cuenta con una *VSI* de perfil ```bx2-4x16``` que se cambia a ```bx2-2x8```.
<br />

3. Después de cambiar el perfil, acepte los cambios en el importe de pago y de click en el botón ```Redimensionar instancia de servidor virtual```.
<br />

4. Espere mientras aparece la nueva configuración y en los tres puntos de click en la opción ```Iniciar``` para poner nuevamente en ejecución la *VSI*.
<br />

<p align="center"><img width="700" src="https://github.com/emeloibmco/VPC-Cambio-Capacidades-Resize/blob/main/Im%C3%A1genes/Reducir%20Tama%C3%B1o.gif"></p>
<br />

Cuando la *VSI* esté lista deberá observar el estado ```En ejecución```.
<br />

<p align="center"><img width="700" src="https://github.com/emeloibmco/VPC-Cambio-Capacidades-Resize/blob/main/Im%C3%A1genes/ReducirOK.PNG"></p>
<br />

## Referencias :mag:
* <a href="https://cloud.ibm.com/docs/vpc?topic=vpc-resizing-an-instance&interface=ui"> Resizing a virtual server instance</a>.
<br />

## Autores :black_nib:
Equipo *IBM Cloud Tech Sales Colombia*.
