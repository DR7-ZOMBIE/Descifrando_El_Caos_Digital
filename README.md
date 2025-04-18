# 🛡️ Descifrando el caos digital: el desafío forense y analista de ciberseguridad

Bienvenidos al desafío forense **"Descifrando el Caos Digital"**. Este proyecto está diseñado para poner a prueba tus habilidades como analista de ciberseguridad, enfrentándote a un ataque complejo que requiere un enfoque estructurado y un análisis técnico detallado. ¿Tienes lo necesario para descifrar el caos digital? ¡Vamos a descubrirlo!

---

## Descarga todos los archivos de reto en el siguiente link:

`URL:` https://drive.google.com/file/d/18Ev30_7YN43Ded_G1JcYoge0WDYMA45E/view?usp=sharing 

## 📁 Contenido del repositorio y orden de trabajo para solucionar:

1. **Página web sospechosa:**  
   - `attack_webpage.html` - Página web posiblemente utilizada en el ataque.
   - `url de acceso:` - https://evento-marzo-ciber-eia-5ae47.web.app/
   - `Los archvios se encuentran en la página en donde se habilita a las 8 p.m para redireccionar al repositorio y poder descargarlos!!!!`
   - `Algo está oculto en la página web en donde accediste al reto, lo necesitas para poder continuar`

2. **Archivo de reglas del firewall:**  
   - `firewall_rules.txt` - Reglas utilizadas durante el ataque.  

3. **Captura de red (Wireshark):**  
   - `network_capture.pcap` - Paquetes de tráfico capturados durante el ataque.  

4. **Archivo cifrado:**  
   - `encrypted_file.enc` - Archivo afectado por el ransomware.  

5. **Imagen de memoria RAM:**  
   - `memory_dump.mem` - Captura forense de la memoria durante el ataque.  

6. **Guía de análisis:**  
   - `guia_ataque.ppt` - Presentación paso a paso para el análisis del ataque.  

---

## 💡 Objetivo del Desafío Forense

1. Reconstruir el ataque y comprender el flujo del incidente.  
2. Correlacionar los datos de la red, la memoria y los archivos para identificar el origen y el método de cifrado.  
3. Extraer todos los **Indicadores de Compromiso (IoCs)** para facilitar la identificación de futuros incidentes similares.  
4. Identificar el ransomware utilizado en el ataque y generar el flag en formato CTF.  
5. Desarrollar un informe forense siguiendo el estándar **NIST SP 800-61**.  

---

## 🔍 Análisis de Proceso Malicioso

### Proceso Malicioso Identificado: [Encuentralos]

### Conexión Maliciosa Detectada: [Encuentralos]

---

## 🧩 Pasos del análisis final en la imagen de memoria RAM 

## Comando y relación volatility2 y volaitlity3

**Cheat sheet guía:** http://blog.onfvp.com/post/volatility-cheatsheet/

1. **Identificación de Procesos:**  
   - Utiliza **pslist** para identificar el proceso malicioso.  
   - Identifica procesos duplicados o inusuales como `Encuentralo!!`.  

2. **Conexiones de Red:**  
   - Analiza el tráfico con **netstat** para determinar las conexiones de la víctima y el atacante.  
   - Verifica los puertos y la IP fuente/destino.  

3. **Análisis de Memoria:**  
   - Usa **malfind** o **ddlist** para identificar modificaciones sospechosas.  
   - Verifica el proceso raíz (PID) y el proceso padre (PPID).  
   - Realiza un análisis de la imagen de memoria con herramientas como **Volatility**.  

4. **Análisis del Ransomware:**  
   - Extraer el proceso malicioso con volaitlity  y verifica el hash en **VirusTotal** o **Hybrid Analysis**.  
   - Usa **CyberChef** para analizar cadenas cifradas.  
   - Genera el hash del malware y realiza una búsqueda en bases de datos de amenazas conocidas.  
   - **Hash del malware:**

5. **Generación del Flag:**  
   - Una vez identificado el nombre del ransomware y sú hash, genera el flag en el siguiente formato:  
     - **CTF{nombre_del_malware&calculo_del_hash_del_malware_SHA-256&nombre_de_la_llave_que_cifro_la_data}**  

---

## 📝 Estructura del Informe Forense  

### **1. Portada**  
- Título: Informe de Análisis Forense Digital  
- Fecha de elaboración  
- Nombre del analista  
- Institución  
- Propósito del informe  

### **2. Resumen Ejecutivo**  
- Breve descripción del incidente  
- Objetivos del análisis  
- Principales hallazgos  
- Conclusiones y recomendaciones  

### **3. Introducción**  
- Descripción del entorno afectado  
- Tipo de ataque identificado  
- Alcance del análisis  

### **4. Metodología**  
- Procedimientos utilizados (según el NIST SP 800-61)  
- Herramientas y técnicas empleadas  
- Justificación de los métodos utilizados  

### **5. Recopilación de Evidencia**  
- Página web sospechosa  
- Reglas del firewall  
- Captura de red (.pcap)  
- Archivo cifrado  
- Imagen de memoria (.mem)  
- Protocolo de manejo y preservación de la evidencia  

### **6. Análisis y Resultados**  
- Identificación del malware alineado a Mitre&Att@ck tácticas, tecnicas y procedimientos utilizados por el cibertacante 
- Análisis de tráfico de red  
- Extracción de IoCs  
- Análisis de memoria volátil  
- Conexión entre el proceso malicioso y el tráfico identificado
- Repesentación visual con estadística y explique cada gráfico porque es vital  

### **7. Conclusiones**  
- Resumen de hallazgos clave  
- Impacto del ataque  
- Probabilidad de compromiso adicional  

### **8. Recomendaciones**  
- Medidas correctivas y preventivas  
- Actualización de políticas de seguridad  
- Refuerzos en los controles de acceso y monitoreo  

### **9. Anexos**  
- Archivos generados durante el análisis  
- Capturas de pantalla relevantes  
- Scripts utilizados  

---

## 🛠️ Herramientas Recomendadas

### **Análisis Web**  
- **CyberChef:** Análisis de cadenas cifradas  
- **VirusTotal:** Escaneo de archivos maliciosos  
- **Hybrid Analysis:** Análisis estático y dinámico  
- **IP Abuse DB:** Verificación de IPs maliciosas  

### **Análisis de Red**  
- **Wireshark:** Inspección de tráfico de red
- **TCPdump:** Inspección de tráfico de red  

### **Análisis de Memoria**  
- **Volatility:** Análisis forense de RAM  
- **Malfind:** Detección de inyecciones de código  
- **Strings:** Extracción de cadenas de texto  
- **File:** Identificación de tipos de archivos
- **Hexeditor:** Análisis hexadecimal 

### **Ingeniería Inversa**  
- **Ghidra:** Desensamblado y análisis binario  
- **CyberChef:** Decodificación de cadenas  
- **OpenSSL:** Verificación de cifrado
- **Adafree:** Desamblado y análisis binario

---

## 🚀 Desafío Final: Flag del CTF  
Una vez identificado el malware, el nombre debe estar envuelto en el formato:  
- **CTF{nombre_del_malware&calculo_del_hash_del_malware_SHA-256&nombre_de_la_llave_que_cifro_la_data}** 

## Descarga todos los archivos de reto en el siguiente link:

`URL:` https://drive.google.com/file/d/18Ev30_7YN43Ded_G1JcYoge0WDYMA45E/view?usp=sharing 

¡Buena suerte, analista! La victoria pertenece a quienes ven patrones donde otros solo ven caos.  
