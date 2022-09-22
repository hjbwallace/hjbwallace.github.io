# hjbwallace.github.io

## Creating the Jekyll template
```
docker run --rm --volume="${pwd}:/srv/jekyll" -it jekyll/jekyll:3.8 sh -c "jekyll new ."
```

## Running the site locally
* Available at https://localhost:4000
* `--force_polling` will make the site rebuild when changes are made

```
docker run --rm --volume="${pwd}:/srv/jekyll" -p 4000:4000 -it jekyll/jekyll:3.8 sh -c "jekyll serve --force_polling" 
```

## Updating Gems
* Make changes in `Gemfile` 
* Run the following command to update `Gemfile.lock`
* Only really required for running locally as GitHib does it's own thing

```
docker run --rm --volume="${pwd}:/srv/jekyll" -it jekyll/jekyll:3.8 sh -c "bundle update"
```

## Minima Theme
https://github.com/jekyll/minima/tree/v2.5.0