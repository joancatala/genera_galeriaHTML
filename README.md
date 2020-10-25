genera_galeriaHTML
==========================

Descripció:
==========================
Tens fotos organitzades per directoris i vols obtenir una galeria HTML molona? aquest és el teu script. Ací tens un exemple de com queda la web resultant: http://galeriahtml.joancatala.net/

Al fitxer **galeriaHTML.tar.gz** tens 3 index.php d'exemple: web amb 3 columnes, amb columnes i amb 9 columnes.

Jo tinc un hortet al terrat, aquest programa em va servir per primera vegada per organitzar-me les fotos de l'hort
que les tinc a http://hortet.joancatala.net , i ara he volgut que aquest script servisca per a altres
galeries HTML que tinc, com per exemple la meua galeria d'astrofotografia http://astrofotografia.joancatala.net
I xim pum.

Requisits:
==========================
doas pkg_add -vi ***ImageMagick***  
doas pkg_add -vi ***Python 3.x***

L'he desenvolupat al meu portàtil (OpenBSD) però mentre tingues Python et funcionarà, a banda de a OpenBSD, a 
Windows, FreeBSD, MacOS X, Linux, etc. 

Funcionament:
==========================
1. Descarrega l'script amb git clone https://github.com/joancatala/genera_galeriaHTML.git   
2. Si no vols escriure la contrasenya constantment: cat ~/.ssh/id_rsa.pub | ssh EL_TEU_USUARI@EL_TEU_SERVIDOR 'cat - >> ~/.ssh/authorized_keys'  
3. Configura el nom del teu usuari i servidor i ruta remota de la teua web (en l'apartat "Configuració")
4. Finalment, executa l'script: python3 ./genera_galeria.py  
