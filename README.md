# Crisp Resume

Crisp Resume is a [Jekyll](https://jekyllrb.com)-based responsive resume template. It draws heavy  inspiration from [Elle Kasai's](https://github.com/ellekasai) [resumecards](https://github.com/ellekasai/resumecards) project, and also from the [Minimal-Mistakes](https://github.com/mmistakes/minimal-mistakes) Jekyll template.

## Background
I loved what Elle did with resumecards; a card is a perfect UI pattern for resume entries. But personally I can't stand Bootstrap - My favorite UI framework is [Semantic UI](http://semantic-ui.com). So when I started building my own resume I decided to use to Semantic UI, and to use [Jekyll collections](https://jekyllrb.com/docs/collections/) for the entries instead of posts, since posts are ordered by date (which doesn't really apply to a resume).

## Using Crisp Resume

It's a good idea to review the [Jekyll documentation](https://jekyllrb.com) if you aren't familiar with it. Then fork this resume, clone it, and run:

`bundle install`

Then `jekyll serve` to launch locally. Your resume will be available at http://localhost:4000

### Customizing
I built the structure here based on my own resume, so you'll want to customize it for your own needs. At a minimum you will want to update:
* `CNAME` if you want to use a custom domain
* `_config.yml` in the project root. This has all of the custom data - the `index.html` is just presentation logic. Be sure to change or blank out the `tracking_id` to use your own Google Analytics.
* Swap out the entries in the various collections that are referenced (they are listed in the `collections` YAML variable), and potentially remove or add other collections depending on your preference.

## Feedback

I'd love to hear what you think! Feel free to drop an issue here in the project or hit me up on [twitter](https://twitter.com/jameswrubel). Find a bug or have an idea for a change? Feel free to send a [pull request](https://help.github.com/articles/using-pull-requests/).
