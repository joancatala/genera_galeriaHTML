genera_galeriaHTML
==========================

Descripció:
==========================
Tens fotos organitzades per directoris i vols obtenir una galeria HTML molona? aquest és el teu script. Ací tens un exemple de com queda la web resultant: http://galeriahtml.joancatala.net/

Al fitxer **galeriaHTML.tar.gz** tens 3 index.php d'exemple: web amb 3 columnes, amb columnes i amb 9 columnes.

<center>
  <h3>Galeria amb 3 columnes</h3>
  <img src="https://raw.githubusercontent.com/joancatala/genera_galeriaHTML/main/captura-3-columnas.jpg" width="650" alt="Exemple de galeria amb 3 columnes"><br />
</center>
  
<center>
  <h3>Galeria amb 6 columnes</h3>
  <img src="https://raw.githubusercontent.com/joancatala/genera_galeriaHTML/main/captura-6-columnas.jpg" width="650" alt="Exemple de galeria amb 6 columnes"><br />
</center>
  
<center>
  <h3>Galeria amb 9 columnes</h3>
  <img src="https://raw.githubusercontent.com/joancatala/genera_galeriaHTML/main/captura-9-columnas.jpg" width="650" alt="Exemple de galeria amb 9 columnes"><br />
</center>

Exemples de galeries:
==========================
- http://hortet.joancatala.net 
- http://astrofotografia.joancatala.net

I bé, ací tens dos exemples del que pots tenir en pocs minuts de manera automàtica.

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

Has de crear un directori anomenat ***fotos-originals*** i deixar els teus directoris i fotos dins. Pots ordenar els directoris a la galeria HTML afegint un número + espai al principi, i el text ha d'estar separat amb guionet. Per exemple, anem a fer una galeria de proves de fotos d'aniversaris:

1 aniversari-30-anys
2 aniversari-31-anys
3 aniversari-del-meu-cosí
4 aniversari-de-la-meua-germana-Ana

I així ja ho tindríes preparat per a tenir una galeria amb 4 directoris ordenats.

Instal·lació i execució:
==========================
1. Descarrega-ho amb: ***git clone https://github.com/joancatala/genera_galeriaHTML.git***   
2. Puja al teu servidor la web ***galeriaHTML.tar.gz*** i descomprimeix-la.
3. Puja la clau SSH al servidor per a no escriure la contrasenya constantment: ***cat ~/.ssh/id_rsa.pub | ssh EL_TEU_USUARI@EL_TEU_SERVIDOR 'cat - >> ~/.ssh/authorized_keys'***  
4. Configura el nom del teu usuari, nom del servidor i la teua ruta remota de la teua web (en l'apartat "Configuració")
5. Finalment, executa l'script: ***python3 ./genera_galeriaHTML.py***  tal i com veuràs a la següent captura de pantalla:

<img src="https://raw.githubusercontent.com/joancatala/genera_galeriaHTML/main/terminal1.jpg" width="650px" alt="" />

Veurem els processos que van ocorreguent:  
<img src="https://raw.githubusercontent.com/joancatala/genera_galeriaHTML/main/terminal2.jpg" width="650px" alt="" />
