import serial

def rgb_to_hex(r, g, b):
    return "#{:02x}{:02x}{:02x}".format(r, g, b)

def main():
    ser = serial.Serial('COMX', 9600)  # Replace 'COMX' with your Arduino's serial port

    while True:
        try:
            line = ser.readline().decode().strip()
            if line:
                r, g, b = map(int, line.split())
                hex_code = rgb_to_hex(r, g, b)
                print(f"Detected color: {hex_code}")
        except KeyboardInterrupt:
            break

    ser.close()

if __name__ == "__main__":
    main()
