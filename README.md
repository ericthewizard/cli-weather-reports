# cli-weather-reports
A command line tool that generates AI-powered weather reports.

## Usage

To use the tool, run the following command:

```bash
weather --style STYLE --tone TONE --temperature TEMP --top_p TOP_P
```

### Arguments

- `--style`: Writing style for the weather report. 
- `--tone`: Writing tone for the weather report. 
- `--temperature`: Sampling temperature for GPT-3 model. A value of `0.0` (default) results in more predictable text, while higher values result in more diverse and potentially unexpected output.
- `--top_p`: Top-p filtering value for GPT-3 model. A value of `1.0` (default) disables top-p filtering, while lower values result in more predictable and coherent text.

### API Keys

This tool uses the following API keys:

- `OPENAI_API_KEY`: Used to access GPT-3.
- `WEATHER_CITY`: City for which to generate weather reports.
- `GEO_KEY`: Used to access the opencagedata API to get latitude and longitude for `WEATHER_CITY`.
- `PIRATE_KEY`: Used to access the Pirate Weather API to get weather data for `WEATHER_CITY`.

## Examples

Here are some example weather reports:

### Simple
```bash
weather
```

```bash
Today's weather will be partly cloudy with a sunrise at 6:52am and a sunset at 5:57pm. The temperature will reach a high of 55 degrees at 10pm and a low of 52 degrees at 2am. The humidity will be at 0.9 and the chance of precipitation is 0.1. The dew point will be at 52 degrees. 

We hope you enjoyed today's weather report and we look forward to bringing you more updates tomorrow.
```

### Custom style and tone
```bash
weather --style poem  --tone excited
```

```bash
The sky is [partly cloudy] and the sun is rising high,
The temperature is [55] degrees, and the humidity is quite nigh.
The dew point is [52] and the precipitation is low,
So the weather today is perfect for a stroll in the snow.

The sun will set at [16:57] and the max temperature will peak,
At [55] degrees, so it's time to go out and take a peek.
The precipitation probability is [0.12] and the max time is at night,
So the weather today is perfect for a picnic in the light.

So don't wait any longer, the weather is just right,
Go out and enjoy the day, and don't forget to take flight.
The weather today is perfect, so don't miss out on the fun,
For there won't be any more updates until tomorrow has come.
```