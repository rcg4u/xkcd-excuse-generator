# XKCD Excuse Generator

Generate your own excuse in a nifty comic style!

[![CircleCI](https://circleci.com/gh/mislavcimpersak/xkcd-excuse-generator/tree/master.svg?style=svg)](https://circleci.com/gh/mislavcimpersak/xkcd-excuse-generator/tree/master)

-----

From this:

![](blank_excuse.png)

to this:

![](example.png)

through simple API!

## Usage

Send `who`, `why` and `what` with desired text as GET parameters to `/v1/excuse`.

Example:
```
https://tyiz03gx7h.execute-api.eu-central-1.amazonaws.com/prod/v1/excuse/?who=0&why=my%20code%20is%20compiling&what=compiling
```

You get the simplest api response in the world:

```
{
    data: {
        image_url: "https://tyiz03gx7h.execute-api.eu-central-1.amazonaws.com/media/30-4d5920434f444520495320434f4d50494c494e47-434f4d50494c494e47.png"
    }
}
```

Follow the given `image_url` value to get your excuse image.

-----

Originaly created for [Python Hrvatska meetup](https://www.meetup.com/Python-Hrvatska/events/242639630/) held on September 12, 2017 and for [Python Belgrade meetup](https://www.meetup.com/PythonBelgrade/events/243547584/) held on September 29, 2017 on which I gave [a talk](https://mislavcimpersak.github.io/serverless-talk/) on serverless technology.

## Tech

Created using [Hug Framework](https://github.com/timothycrosley/hug), packaged with [Zappa](https://github.com/Miserlou/Zappa/) and served from AWS Lambda.

## Legal

### Original image

[Original image](https://xkcd.com/303/) created by Randall Munroe from XKCD.

Released under [Creative Commons Attribution-NonCommercial 2.5 License](https://creativecommons.org/licenses/by-nc/2.5/).

### Font

[XKCD-Font](https://github.com/ipython/xkcd-font) created by iPython team.

Released under [Creative Commons Attribution-NonCommercial 3.0 License](https://creativecommons.org/licenses/by-nc/3.0/).

