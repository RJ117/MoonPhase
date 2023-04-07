# MoonPhase

import ephem
import datetime

def moon_phase(date):
    moon = ephem.Moon(date)
    phase = moon.moon_phase
    return phase

def main():
    date = datetime.datetime.now()  # Use current date and time
    phase = moon_phase(date)

    if 0.0 <= phase < 0.1:
        print("New Moon")
    elif 0.1 <= phase < 0.25:
        print("Waxing Crescent")
    elif 0.25 <= phase < 0.45:
        print("First Quarter")
    elif 0.45 <= phase < 0.55:
        print("Waxing Gibbous")
    elif 0.55 <= phase < 0.65:
        print("Full Moon")
    elif 0.65 <= phase < 0.75:
        print("Waning Gibbous")
    elif 0.75 <= phase < 0.85:
        print("Last Quarter")
    else:
        print("Waning Crescent")

if __name__ == "__main__":
    main()
    
    python moon_phase.py
