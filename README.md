# ConferenceCarbonTracker
Tracking the carbon emissions from scientific conferences.

## How to add new conferences

### Option 1: Travel Footprint Calculator

Use the [Travel Footprint Calculator](https://travel-footprint-calculator.irap.omp.eu/) and check the box `add conference to ConferenceCarbonTracker`.

### Option 2: Via ConferenceCarbonTracker.com

Use the `add conference` button and provide the data.

### Option 3: Create a pull request

Create a pull request to this repository to add a file to `/conferences`, named as `shortName_year_randomString.JSON`, e.g. like `agu_2019_kQ1e6Iaa.JSON`. This JSON file should have at least the following fields

```JSON
{
    "shortName": "AGU",
    "longName": "American Geophysical Union",
    "website": "https://www.agu.org/Fall-Meeting-2019",
    "date": {
        "year": 2019,
        "month": 12,
        "day": 9,
        "lengthInDays": 5
    },  
    "location": {
        "city": "San Francisco",
        "country": "USA"
    },
    "attendees": {
        "total": 28000,
        "virtual": 0,
        "in-person": 28000
    },
    "carbonFootprint": {
        "unit": "tCO2",
        "emissions": 80000,
        "reference": "https://www.nature.com/articles/d41586-020-02057-2"
    }
  }
  ```