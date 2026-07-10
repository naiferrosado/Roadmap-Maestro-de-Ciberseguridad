# 🛡️ Roadmap Maestro de Ciberseguridad
### Fusión analizada de 3 roadmaps (visual por fases + Ultimate Mastery Roadmap + esquema técnico detallado)

> Este roadmap combina lo mejor de 3 fuentes distintas:
>
> - **Fuente 1 — [GeeksforGeeks: Cybersecurity Roadmap](https://www.geeksforgeeks.org/cybersecurity/cybersecurity-roadmap/):** la mejor secuencia lógica por fases (5 niveles claros).
> - **Fuente 2 — [Hamed233/Cybersecurity-Mastery-Roadmap (GitHub)](https://github.com/Hamed233/Cybersecurity-Mastery-Roadmap):** el catálogo más completo de libros, cursos, herramientas y certificaciones.
> - **Fuente 3 — [roadmap.sh/cyber-security](https://roadmap.sh/cyber-security):** el detalle granular de conceptos que las otras dos mencionan pero no explican (terminología de redes, tipos de ataques, comandos, protocolos).
>
> Están ordenadas por **dependencia real de conocimiento**: no se puede entender OWASP sin TCP/IP, no se puede hacer threat hunting sin SIEM, no se puede hacer forense sin entender el sistema de archivos, etc.

---

## 🧭 Cómo usar este roadmap

Cada fase tiene:

- **Objetivo** — qué deberías poder hacer al terminarla
- **Temas** — el contenido técnico a dominar
- **Herramientas** — con qué practicar
- **Recursos** — cursos/libros más recomendados (curados, no la lista completa)
- **Hito de dominio** — cómo saber que ya puedes avanzar
- **Tiempo estimado** — dedicando 10-15h/semana

No hace falta dominar el 100% de cada fase antes de avanzar — el 70-80% es suficiente para seguir, porque muchos temas se refuerzan en las fases siguientes.

---

## FASE 0 — Fundamentos de IT (la base que todos dan por hecho)

**Objetivo:** Entender cómo funciona una computadora y un sistema operativo antes de intentar asegurarlos.

**Temas:**

- Componentes de hardware y su función (CPU, RAM, almacenamiento, buses)
- Tipos de conexión (USB, HDMI, Ethernet, etc.) y su propósito
- Sistemas operativos: Windows, Linux, macOS — instalación, versiones, diferencias
- Navegación por GUI y CLI
- Permisos de usuario y sistema de archivos
- Instalación de software y gestión de aplicaciones
- Operaciones CRUD sobre archivos (crear, leer, modificar, borrar)
- Troubleshooting básico independiente del OS
- Suites ofimáticas (MS Office, Google Suite, iCloud) — solo lo esencial
- Conectividad inalámbrica: WiFi, Bluetooth, NFC, Infrarrojo

**Herramientas:** VirtualBox, VMware Player

**Recursos:**

- CS50: Introduction to Computer Science
- "Computer Systems: A Programmer's Perspective" — Bryant & O'Hallaron
- **CompTIA A+ (220-1201/1202) — Professor Messer (curso oficial recomendado):**
  - [A+ 220-1201 (Core 1) — Professor Messer](https://youtube.com/playlist?list=PLG49S3nxzAnnes8ZGI-OBlKEukHCX46N8)
  - [A+ 220-1202 (Core 2) — Professor Messer](https://youtube.com/playlist?list=PLG49S3nxzAnn7PDGQ17m5AYbDRhnW7vOb)

**Hito de dominio:** Puedes instalar un SO desde cero, navegar por terminal sin depender del mouse, y explicar qué hace cada componente de una PC.

**Tiempo estimado:** 2-3 semanas (menos si ya tienes experiencia previa en IT o estudias una carrera afín, como Sistemas o Informática)

---

## FASE 1 — Redes (el 40% de la ciberseguridad ocurre aquí)

**Objetivo:** Entender cómo viaja la información entre sistemas — sin esto, nada de seguridad tiene sentido.

**Temas:**

- Modelo OSI y arquitectura TCP/IP
- Direccionamiento IP: IPv4/IPv6, subnetting, CIDR, máscara de subred, gateway por defecto
- IP pública vs privada, localhost, loopback
- Protocolos comunes y sus puertos: HTTP/HTTPS, DNS, FTP/SFTP, SSH, RDP
- SSL/TLS — fundamentos (no criptografía profunda aún)
- Terminología esencial: VLAN, DMZ, ARP, NAT, DHCP, DNS, VPN
- Topologías de red: estrella, anillo, malla, bus
- Diferencias LAN, WAN, MAN, WLAN
- Conceptos de NAS y SAN
- Virtualización: hipervisor, VM, GuestOS vs HostOS

**Herramientas:**

- Wireshark (análisis de paquetes)
- tcpdump (captura por línea de comandos)
- Cisco Packet Tracer / GNS3 (simulación de redes)
- Herramientas de diagnóstico: `ping`, `nslookup`, `dig`, `traceroute/tracert`, `ipconfig`/`ifconfig`, `netstat`, `route`, `arp`

**Recursos:**

- Computer Networking: A Top-Down Approach
- Stanford CS144: Computer Networking
- Practical Networking (sitio web)
- "TCP/IP Illustrated, Volume 1" — W. Richard Stevens
- **CompTIA Network+ (N10-009) — curso oficial recomendado:**
  - [Network+ N10-009 — Professor Messer](https://youtube.com/playlist?list=PLG49S3nxzAnl_tQe3kvnmeMid0mjF8Le8)
  - [Network+ N10-009 — curso animado completo (PowerCert)](https://youtu.be/CY4hn70K3r8)

**Práctica:**

- Simular redes en GNS3/Packet Tracer
- Capturar y analizar tráfico real con Wireshark
- Practicar subnetting hasta poder hacerlo mentalmente
- Configurar reglas básicas de firewall

**Hito de dominio:** Puedes explicar el recorrido completo de un paquete desde que escribes una URL hasta que ves la página, y puedes calcular subredes sin calculadora.

**Tiempo estimado:** 4-6 semanas

---

## FASE 2 — Linux y Línea de Comandos

**Objetivo:** Moverte con soltura en Linux, porque es el sistema operativo de facto en seguridad ofensiva, defensiva y servidores.

**Temas:**

- Instalación y configuración de distros (Ubuntu, Kali, Arch)
- Sistema de permisos (`chmod`, `chown`, usuarios/grupos)
- Gestión de procesos y servicios
- Administración básica de Linux
- Bash scripting para automatización

**Herramientas:** Kali Linux, VirtualBox/Vagrant

**Recursos:**

- Linux Journey
- OverTheWire: Bandit (wargame práctico, muy recomendado por su enfoque hands-on)
- "The Linux Command Line" — William Shotts

**Práctica:**

- Completar todos los niveles de OverTheWire: Bandit
- Configurar un stack LAMP/LEMP
- Escribir 3-5 scripts bash que automaticen tareas reales (backups, monitoreo de logs, etc.)

**Hito de dominio:** Puedes resolver un problema en un servidor Linux sin buscar cada comando en Google.

**Tiempo estimado:** 3-4 semanas (en paralelo con Fase 1 es válido)

---

## FASE 3 — Programación para Seguridad

**Objetivo:** No necesitas ser desarrollador, pero sí necesitas leer y escribir scripts para automatizar y entender exploits/herramientas.

**Temas:**

- Python (prioridad #1 — la mayoría de herramientas de seguridad están en Python)
- Bash / PowerShell (automatización en Linux/Windows)
- Nociones de JavaScript (para entender ataques web como XSS)
- Nociones de Go (cada vez más usado en herramientas modernas de seguridad)

**Recursos:**

- Python for Everybody
- Automate the Boring Stuff with Python
- "Black Hat Python" — Justin Seitz (cuando llegues a fases ofensivas)

**Práctica:**

- Construir un port scanner simple en Python
- Construir un generador de contraseñas
- Automatizar una tarea repetitiva de tu día a día (correo, archivos, backups, reportes, etc.)

**Hito de dominio:** Puedes leer el código fuente de una herramienta de seguridad open source y entender qué hace, línea por línea.

**Tiempo estimado:** Continuo — 3-4 semanas iniciales, luego se refuerza en cada fase siguiente

---

## FASE 4 — Fundamentos de Seguridad de la Información

**Objetivo:** Aprender el marco conceptual que sostiene todo lo demás.

**Temas:**

- Tríada CIA (Confidencialidad, Integridad, Disponibilidad)
- Autenticación vs Autorización
- Métodos de autenticación: Kerberos, RADIUS, LDAP, SSO, MFA/2FA, certificados
- Criptografía básica: hashing, salting, intercambio de llaves, PKI, llaves públicas/privadas, ofuscación
- Defensa en profundidad (Defense in Depth)
- Zero Trust — conceptos centrales
- Perímetro vs DMZ vs segmentación
- Riesgo: definición y evaluación básica
- Backups y resiliencia
- Cyber Kill Chain y Diamond Model
- Frameworks: MITRE ATT&CK, NIST, ISO 27001, CIS CSF

**Herramientas:** CyberChef, OpenSSL, Hashcat

**Recursos:**

- NIST Cybersecurity Framework
- "Security Engineering" — Ross Anderson
- Cryptography I — Stanford (Coursera)
- **CompTIA Security+ (SY0-701) — curso oficial recomendado:**
  - [Security+ SY0-701 — Professor Messer](https://youtube.com/playlist?list=PLG49S3nxzAnl4QDVqK-hOnoqcSKEIDDuv)
  - [Security+ SY0-701 — curso alternativo completo (BurningIceTech)](https://youtube.com/playlist?list=PLc6LqxQFwub864EdhbzrTGkE1xeW5WE8E)

**Práctica:**

- Analizar 2-3 casos reales de brechas de seguridad (breach post-mortems)
- Crear una política de seguridad para una organización ficticia
- Resolver retos básicos de criptografía en Cryptopals

**Hito de dominio:** Puedes explicar cualquier incidente de seguridad usando el vocabulario correcto de estos frameworks.

**Tiempo estimado:** 4-5 semanas

**🎯 Certificación recomendada en este punto: CompTIA Security+**

---

## FASE 5 — Herramientas de Reconocimiento y Análisis

**Objetivo:** Dominar las herramientas que vas a usar todos los días, sin importar si vas por Red o Blue Team.

**Temas:**

- Reconocimiento y OSINT
- Escaneo de puertos y servicios
- Análisis de vulnerabilidades
- Sniffing de paquetes y análisis de protocolos

**Herramientas clave:**

- **Nmap** — escaneo de red (el más importante de todos)
- **Wireshark** — análisis profundo de paquetes
- **Shodan** — buscador de dispositivos expuestos en internet
- **theHarvester / Recon-ng** — recolección OSINT
- **OpenVAS / Nessus Essentials** — escaneo de vulnerabilidades

**Recursos:**

- Nmap official guide
- SANS SEC504: Hacker Tools, Techniques, Exploits, and Incident Handling

**Práctica:**

- Levantar Metasploitable (máquina vulnerable) y escanearla completa con Nmap
- Hacer un reporte de vulnerabilidades básico sobre esa máquina

**Hito de dominio:** Puedes hacer un reconocimiento completo de una red/host y documentar hallazgos como lo haría un profesional.

**Tiempo estimado:** 2-3 semanas

---

## FASE 6 — Seguridad de Aplicaciones Web

**Objetivo:** Entender cómo se rompen las aplicaciones web — esencial incluso si tu meta es SOC, porque la mayoría de alertas que vas a triagear vienen de ataques web.

**Temas (en orden de aparición en el mundo real):**

- OWASP Top 10 completo (memorizar y entender cada uno, no solo el nombre)
- SQL Injection (SQLi)
- Cross-Site Scripting (XSS)
- Cross-Site Request Forgery (CSRF)
- Directory Traversal
- Buffer Overflow (concepto, aunque profundizarás en fases avanzadas)

**Herramientas:**

- Burp Suite (Community Edition está bien para empezar)
- OWASP ZAP
- SQLmap
- DVWA / OWASP Juice Shop (apps vulnerables para practicar legalmente)

**Recursos:**

- PortSwigger Web Security Academy (gratis, es el estándar de la industria)
- OWASP Top Ten (owasp.org)
- "The Web Application Hacker's Handbook" — Stuttard & Pinto

**Práctica:**

- Completar todos los labs de PortSwigger de nivel "Apprentice"
- Explotar DVWA en sus 4 niveles de dificultad

**Hito de dominio:** Puedes identificar y explotar cada vulnerabilidad del OWASP Top 10 en un entorno controlado, y explicar cómo prevenirla en código, sin importar el framework o lenguaje que uses.

**Tiempo estimado:** 4-6 semanas

---

## FASE 7 — Bifurcación: Blue Team vs Red Team

A partir de aquí el camino se divide. La recomendación general es no elegir a ciegas: prueba ambas rutas durante 2-3 semanas cada una (con CTFs beginner-friendly) antes de decidir dónde especializarte. Dicho esto, entender cómo atacan es indispensable para defender bien, y viceversa — nadie domina una ruta ignorando por completo la otra.

### 🔵 Ruta Defensiva (Blue Team / SOC)

**Temas:**

- Arquitectura de un SOC (Security Operations Center)
- SIEM: qué es, cómo funciona, cómo se configuran reglas de detección
- Análisis y correlación de logs
- IDS/IPS: Snort, Suricata
- Threat Hunting — conceptos y metodología
- Threat Intelligence y OSINT aplicado a defensa
- Proceso de Respuesta a Incidentes: Preparación → Identificación → Contención → Erradicación → Recuperación → Lecciones Aprendidas
- Clasificación de amenazas: Zero Day, APT, conocidas vs desconocidas
- Falsos positivos/negativos, verdaderos positivos/negativos
- Honeypots
- Hardening de sistemas: NAC, bloqueo de puertos, GPO, ACLs, parcheo

**Herramientas clave:**

- **Splunk** — SIEM líder de la industria
- **Wazuh / ELK Stack (Elastic + Kibana)** — alternativa open source, ideal para tu home lab
- **Security Onion** — plataforma completa de monitoreo
- **TheHive + MISP** — gestión de incidentes y threat intel
- **Sysmon** — monitoreo avanzado en Windows
- **YARA** — detección de patrones de malware

**Recursos:**

- Blue Team Labs Online
- "Blue Team Handbook: SOC, SIEM and Threat Hunting" — Don Murdoch
- SANS SEC450: Blue Team Fundamentals

**Práctica (proyecto estrella de portafolio):**

- Montar un home lab con Wazuh o Splunk Free
- Generar tráfico de ataque simulado y crear reglas de detección
- Documentar 3-5 "casos de incidente" simulados con tu proceso completo de respuesta

**🎯 Certificaciones:** CompTIA CySA+, GIAC GCIH

### 🔴 Ruta Ofensiva (Red Team / Pentesting)

**Temas:**

- Metodología de pentesting (PTES)
- Explotación con Metasploit
- Escalación de privilegios
- Ingeniería social (conceptual, con permiso explícito para práctica)
- LOLBAS — uso de herramientas legítimas del sistema con fines maliciosos

**Herramientas:** Metasploit, Hydra, John the Ripper, Hashcat, Mimikatz

**Recursos:** TryHackMe, HackTheBox, "The Hacker Playbook 3"

**🎯 Certificación:** OSCP (la más respetada, pero exige mucha práctica previa)

**Hito de dominio (ambas rutas):** Puedes participar en un CTF beginner-friendly (picoCTF, TryHackMe) y resolver al menos el 60% de los retos sin ayuda externa.

**Tiempo estimado:** 8-12 semanas

---

## FASE 8 — Nube y Contenedores

**Objetivo:** La infraestructura moderna vive en la nube — sin esto, cualquier perfil de ciberseguridad queda incompleto.

**Temas:**

- Modelos de servicio: IaaS, PaaS, SaaS
- Modelos de despliegue: público, privado, híbrido
- Diferencias entre on-premises y cloud
- Infrastructure as Code (concepto)
- Seguridad en AWS/Azure/GCP (elige uno para profundizar — AWS tiene más demanda laboral)
- Seguridad de contenedores: Docker, Kubernetes

**Herramientas:**

- AWS Security Hub / Prowler (auditoría de AWS)
- Trivy (escaneo de vulnerabilidades en contenedores)
- Falco (seguridad en runtime de contenedores)

**Recursos:**

- AWS Security Fundamentals (curso gratuito)
- "Practical Cloud Security" — Chris Dotson

**Hito de dominio:** Puedes explicar el modelo de responsabilidad compartida en la nube y detectar una mala configuración común (ej. un bucket S3 público).

**Tiempo estimado:** 3-4 semanas

---

## FASE 9 — Especializaciones Avanzadas (elige 1-2, no todas)

Ya con la base sólida, aquí es donde te vuelves experto en algo específico. Elige según tu ruta: si vas por Blue Team/SOC, Forense Digital y Análisis de Malware son las más naturales; si vas por Red Team, DevSecOps y Cloud Security suelen tener más demanda.

| Especialización | Por qué te serviría | Herramientas clave |
|---|---|---|
| **Forense Digital** | Complementa perfecto al SOC — cuando hay un incidente, alguien tiene que investigar qué pasó | Autopsy, Volatility, FTK Imager |
| **Análisis de Malware** | Entender qué hace el malware que tu SOC detecta | Ghidra, Cuckoo Sandbox, REMnux, any.run |
| **DevSecOps** | Integrar seguridad en pipelines CI/CD — alta demanda | SonarQube, Snyk, OWASP Dependency-Check |
| **Cloud Security** | Si te inclinas más hacia infraestructura que hacia SOC tradicional | Prowler, ScoutSuite, Pacu |
| **Threat Intelligence** | Evolución natural de un SOC Analyst senior | MISP, OpenCTI, MITRE ATT&CK Navigator |

**Recursos según elección:** ver la sección de recursos curados al final del documento.

**Tiempo estimado:** 6-8 semanas por especialización

---

## FASE 10 — Práctica Continua y Comunidad

Esto no es una fase que termina — es el hábito que mantienes para siempre.

**CTFs (en orden de dificultad):**

1. picoCTF (principiante absoluto)
2. TryHackMe (aprendizaje guiado)
3. HackTheBox (más desafiante, sin guía)
4. CTFtime.org (calendario de competencias en vivo)

**Comunidades:**

- Reddit: r/cybersecurity, r/AskNetsec, r/netsec
- Discord de TryHackMe
- Women in Cybersecurity (WiCyS) — si aplica a tu red de contactos
- OWASP chapters locales (revisa si hay comunidad en RD)

**Consumo continuo:**

- Blogs: Krebs on Security, The Hacker News, BleepingComputer
- YouTube: IppSec (walkthroughs de HackTheBox), John Hammond, NetworkChuck
- Newsletters de seguridad semanales

---

## 📜 Ruta de Certificaciones Recomendada (orden ideal para ti)

| Orden | Certificación | Cuándo tomarla | Por qué |
|---|---|---|---|
| 1 | **CompTIA Security+** | Después de Fase 4 | Estándar de entrada, la piden en casi todas las vacantes junior |
| 2 | **CompTIA CySA+** | Después de Fase 7 (Blue Team) | Enfocada 100% en detección y respuesta — perfecta para SOC |
| 3 | **GIAC GCIH** | Con experiencia práctica en incident response | Reconocida y técnica, sube tu perfil sobre CySA+ |
| Opcional | **CEH** | Si quieres balance ofensivo/defensivo | Amplia pero menos técnica que OSCP |
| Avanzado | **OSCP** | Solo si te inclinas fuerte hacia pentesting | La más respetada en el mundo ofensivo, requiere examen práctico de 24h |

---

## 🗂️ Recursos Curados por Categoría (lo mejor de las 3 fuentes, sin duplicados)

**Libros esenciales (en orden de lectura):**

1. "Cybersecurity for Beginners" — Raef Meeuwisse
2. "Computer Security: Principles and Practice" — William Stallings
3. "The Web Application Hacker's Handbook" — Stuttard & Pinto
4. "Blue Team Handbook" — Don Murdoch
5. "Practical Malware Analysis" — Sikorski & Honig (cuando llegues a esa especialización)

**Plataformas de práctica imprescindibles:**

- TryHackMe (mejor punto de partida)
- HackTheBox (cuando ya tengas base)
- PortSwigger Web Security Academy (gratis, obligatorio para web)
- OverTheWire (para Linux/fundamentos)

**Labs vulnerables para montar en casa:**

- Metasploitable
- DVWA
- OWASP Juice Shop

---

## ⏱️ Línea de Tiempo Total Estimada

- **Fases 0-4 (fundamentos):** ~4 meses
- **Fases 5-7 (herramientas + especialización SOC/pentesting):** ~4 meses
- **Fases 8-9 (nube + especialización avanzada):** ~2-3 meses
- **Total hasta perfil empleable junior:** ~10-12 meses de estudio constante (10-15h/semana)

Si prefieres, puedes desglosar cada fase en un plan semana a semana con objetivos concretos — eso ayuda mucho a mantener el ritmo en un roadmap tan largo.

---

## 🙏 Créditos y Fuentes

Este roadmap fue construido analizando, reordenando y fusionando el contenido de las siguientes 3 fuentes. Todo el mérito del contenido original es de sus respectivos autores:

1. **[GeeksforGeeks — Cybersecurity Roadmap](https://www.geeksforgeeks.org/cybersecurity/cybersecurity-roadmap/)**
2. **[Hamed233 — Cybersecurity-Mastery-Roadmap (GitHub)](https://github.com/Hamed233/Cybersecurity-Mastery-Roadmap)**
3. **[roadmap.sh — Cyber Security](https://roadmap.sh/cyber-security)**

Este documento no pretende reemplazar ninguna de las 3 fuentes originales, sino ofrecer una versión reorganizada por dependencia lógica de conocimiento, con detalles adicionales de tiempos estimados, hitos de dominio y orden de certificaciones.
