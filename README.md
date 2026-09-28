# Transformer-fault-alarm
# Transformer Fault Alarm System

MIN_VOLTAGE = 200
MAX_VOLTAGE = 250
MAX_CURRENT = 100
MAX_TEMPERATURE = 90

print("==============================")
print("      TRANSFORMER FAULT ALARM")
print("==============================")

voltage = float(input("Enter transformer voltage (V): "))
current = float(input("Enter transformer current (A): "))
temperature = float(input("Enter transformer temperature (°C): "))

fault = False

print("\n--- Transformer Monitoring ---")
print("Voltage    :", voltage, "V")
print("Current    :", current, "A")
print("Temperature:", temperature, "°C")

# Voltage check
if voltage < MIN_VOLTAGE:
    print("⚠️ Under-voltage fault")
    fault = True

elif voltage > MAX_VOLTAGE:
    print("⚠️ Over-voltage fault")
    fault = True

# Current check
if current > MAX_CURRENT:
    print("⚠️ Overcurrent fault")
    fault = True

# Temperature check
if temperature > MAX_TEMPERATURE:
    print("⚠️ Transformer overheating")
    fault = True

# Alarm
if fault:
    print("\n🔴 TRANSFORMER FAULT DETECTED")
    print("🚨 ALARM: ON")
    print("⚠️ Protection system activated")

else:
    print("\n🟢 TRANSFORMER STATUS: NORMAL")
    print("🔕 ALARM: OFF")
    print("✅ No fault detected")
