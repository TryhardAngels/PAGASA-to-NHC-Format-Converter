# PAGASA to NHC Bulletin Converter

Convert Philippine PAGASA typhoon bulletins to National Hurricane Center (NHC) format.

## Features

- Converts PAGASA bulletin format to NHC format
- Automatic time conversion (Philippines Time to UTC)
- Wind speed conversion (km/h to mph with rounding)
- Pressure conversion (hPa to inches)
- Direction abbreviation (e.g., "North Northwest" → "NNW")
- Distance conversion (kilometers to miles)
- Auto-detects when bulletin is complete

## Usage

1. Run the script:
```bash
python3 pagasa_nhc_converter.py
```

2. Paste your PAGASA bulletin text

3. Hit enter

4. The script automatically converts and displays the NHC format

## Example

**Input (PAGASA format):**
```
LIFE-THREATENING CONDITIONS CONTINUE OVER BICOL REGION AS "UWAN" CONTINUES TO MOVE
WEST NORTHWESTWARD OVER THE COASTAL WATERS OF CAMARINES NORTE.
Location of Center (1:00 PM)
The center of the eye of Super Typhoon UWAN was estimated at 135 km North Northwest of Virac,
Catanduanes or 100 km Northeast of Daet, Camarines Norte (14.7°N, 123.7°E)
Intensity
Maximum sustained winds of 185 km/h near the center,
gustiness of up to 230 km/h, and central pressure of 935 hPa
Present Movement
West northwestward at 30 km/h
```

**Output (NHC format):**
```
...LIFE-THREATENING CONDITIONS CONTINUE OVER BICOL REGION AS "UWAN" CONTINUES TO MOVE WEST NORTHWESTWARD OVER THE COASTAL WATERS OF CAMARINES NORTE....


SUMMARY OF 1300 PHT...0500 UTC...INFORMATION
----------------------------------------------
LOCATION...14.7N 123.7E
ABOUT 83 MI...135 KM NNW OF VIRAC, CATANDUANES
ABOUT 62 MI...100 KM NE OF DAET, CAMARINES NORTE
MAXIMUM SUSTAINED WINDS...115 MPH...185 KM/H
PRESENT MOVEMENT...WNW OR 292 DEGREES AT 19 MPH...30 KM/H
MINIMUM CENTRAL PRESSURE...935 MB...27.61 INCHES
```

## Conversions

- **Time**: Philippines Time (UTC+8) → UTC
- **Wind Speed**: km/h → mph (rounded to nearest 5 mph for sustained winds)
- **Movement Speed**: km/h → mph (rounded to nearest mph)
- **Distance**: kilometers → miles
- **Pressure**: hPa/mb → inches of mercury
- **Direction**: Full text → Standard abbreviations (N, NE, E, SE, S, SW, W, NW, NNW, etc.)

## Requirements

- Python 3.6+
- No external dependencies (uses only standard library)

## License

MIT License - Feel free to use and modify as needed.
