# LeDommage

## Descripción

LeDommage es una herramienta de ataque DoS (Denial of Service) desarrollada por Vanille Systems en 2025. Permite realizar ataques ICMP Flood a una IP o dominio especificado.

**Advertencia:** El uso de esta herramienta para realizar ataques DoS es ilegal y puede acarrear consecuencias legales graves. Utiliza esta herramienta bajo tu propia responsabilidad y únicamente en entornos controlados con fines de prueba y aprendizaje (o no 😉)

## Instalación

1.  Asegúrate de tener `hping3` instalado en tu sistema. Si no lo tienes, puedes instalarlo utilizando la opción 1 del menú.

    ```bash
    sudo apt-get install hping3 -y
    ```

## Uso

1.  Ejecuta el script `ledommage.py`.
2.  Selecciona la opción 2 del menú ("Launch DoS attack whit LeDommage").
3.  Introduce la IP o el dominio al que deseas enviar el ataque.
4.  El script ejecutará `hping3` con los parámetros necesarios para realizar un ataque ICMP Flood.

**Parámetros de `hping3` utilizados:**

*   `--icmp`: Especifica el uso de paquetes ICMP.
*   `-a '8.8.8.8'`:  Establece la dirección IP de origen del paquete como `8.8.8.8` (DNS de Google). **Nota:** Esta opción podría ser modificada para suplantar otra IP de origen.
*   `-e 'dommage'`: Incluye el payload "dommage" en el paquete ICMP.
*   `--flood`: Envía los paquetes lo más rápido posible.

**Ejemplo de uso:**

```bash
python ledommage.py
