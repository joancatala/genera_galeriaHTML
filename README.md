genera_galeriaHTML
==========================

Descripció:
==========================
Tens fotos organitzades per directoris i vols obtenir una galeria HTML molona? aquest és el teu script. Ací tens un exemple de com queda la web resultant: http://galeriahtml.joancatala.net/

Al fitxer **galeriaHTML.tar.gz** tens 3 index.php d'exemple: web amb 3 columnes, amb columnes i amb 9 columnes.

  <center>
  <h3>Galeria amb 3 columnes</h3>
  <img src="https://raw.githubusercontent.com/joancatala/genera_galeriaHTML/main/captura-3-columnas.jpg" width="400" alt="Exemple de galeria amb 3 columnes"><br />
  </center>
  
  <center>">
  <h3>Galeria amb 6 columnes</h3>
  <img src="https://raw.githubusercontent.com/joancatala/genera_galeriaHTML/main/captura-6-columnas.jpg" width="400" alt="Exemple de galeria amb 6 columnes"><br />
  </center>
  
  <center>
  <h3>Galeria amb 9 columnes</h3>
  <img src="https://raw.githubusercontent.com/joancatala/genera_galeriaHTML/main/captura-9-columnas.jpg" width="400" alt="Exemple de galeria amb 9 columnes"><br />
  </center>

Jo tinc un hortet al terrat, aquest programa em va servir per primera vegada per organitzar-me les fotos de l'hort que les tinc a http://hortet.joancatala.net , i ara he volgut que aquest script servisca per a altres galeries HTML que tinc, com per exemple la meua galeria d'astrofotografia http://astrofotografia.joancatala.net
I xim pum.

Requisits:
==========================
Jo ho he desenvolupat a OpenBSD, però pots fer-ho a qualsevol altre sistema operatiu amb aquest programari:

doas pkg_add -vi ***ImageMagick***  
doas pkg_add -vi ***Python 3.x***

Funcionament:
==========================
Aquest programari agafa el títol dels teus directoris i genera una galeria HTML i després obtindràs una web bootstrap amb CSS3 molt xula i responsive amb la teua galeria d'imatges. L'script comprimirà en tar.gz la galeria i la publicarà al teu servidor web, per això a la part de configuració has de ficar:
- el teu usuari (de l'SSH/SCP).
- el nom del servidor.
- la ruta de l'espai web remot on tindràs publicada la galeria.

Instal·lació i execució:
==========================
1. Descarrega-ho amb: git clone https://github.com/joancatala/genera_galeriaHTML.git   
2. Puja la clau SSH al servidor per a no escriure la contrasenya constantment: cat ~/.ssh/id_rsa.pub | ssh EL_TEU_USUARI@EL_TEU_SERVIDOR 'cat - >> ~/.ssh/authorized_keys'  
3. Configura el nom del teu usuari, nom del servidor i la teua ruta remota de la teua web (en l'apartat "Configuració")
4. Finalment, executa l'script: python3 ./genera_galeria.py  
