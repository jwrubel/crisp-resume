# Crisp Resume

Crisp Resume is a [Jekyll](https://jekyllrb.com)-based responsive resume template. It draws heavy  inspiration from [Elle Kasai's](https://github.com/ellekasai) [resumecards](https://github.com/ellekasai/resumecards) project, and also from the [Minimal-Mistakes](https://github.com/mmistakes/minimal-mistakes) Jekyll template.

## Background
I loved what Elle did with resumecards; a card is a perfect UI pattern for resume entries. But personally I can't stand Bootstrap - My favorite UI framework is [Semantic UI](http://semantic-ui.com). So when I started building my own resume I decided to use to Semantic UI, and to use [Jekyll collections](https://jekyllrb.com/docs/collections/) for the entries instead of posts, since posts are ordered by date (which doesn't really apply to a resume).

## Using Crisp Resume

It's a good idea to review the [Jekyll documentation](https://jekyllrb.com) if you aren't familiar with it. Then fork this resume, clone it, and run:

`bundle install`

Then `jekyll serve` to launch locally. Your resume will be available at http://localhost:4000

There are two branches in this project; `master` and `gh-pages` The master branch just has greeked text to give you an idea of what data you should enter. On the gh-pages branch I implemented Eugene Mirman's hilarious [LinkedIn profile](https://www.linkedin.com/in/eugene-mirman-bb023396) using Crisp Resume, to give an idea of what a 'real world' profile might look like. For additional inspiration you can also use [my resume](http://james.wrubel.org) which also uses Crisp Resume.

Per the [GitHub documentation](https://help.github.com/articles/user-organization-and-project-pages/), if you want to use Crisp Resume as your User or Organization Page, do your editing on the master branch. If you want to use it as a Project Page, use the gh-pages branch.

## Customizing
To implement your own resume, fork the project and switch to the branch you want. Everyone's experience is different, and you may want to highlight different aspects of your professional experience. Crisp Resume is extremely flexible and all of the content is separated from the layout. At a minimum you will want to update:
* `_config.yml` in the project root. This has all of the custom data - the `index.html` is just presentation logic. Be sure to enter the `tracking_id` if you want to use your own Google Analytics.
* Swap out the entries in the various collections that are referenced (they are listed in the `collections` YAML variable), and potentially remove or add other collections depending on your preference.
* Replace the headshot and any other images in the `/images` directory
* [OPTIONAL] Add a `CNAME` file if you want to use a custom domain (See GitHub's [documentation](https://help.github.com/articles/using-a-custom-domain-with-github-pages/) on this if you are not sure how)

### A special note on printing
I'll be the first to admit, having a printable version of this would be awesome. I worked on that for a while, and Semantic UI actually looks pretty good by default when printed. But, [CSS being awesome](http://imgur.com/gallery/9qzBYbH), getting page breaks to line up is next to impossible. And personally, I want different things on a printed resume than on the web. So I just implemented it as a PDF (there's an example on the master branch). It won't show unless you have one set in your `_config.yml`.

### Managing Sections
Crisp Resume is designed to be extensible. It includes a set of sections implemented as Jekyll Collections. The default sections are:
* employment (used for Work History)
* education (used for formal education experience)
* skills (used for ranking your ability at things employers may be looking for)
* publications (used for papers, presentations, etc)
* errata (used for anything that doesn't fit another section)

Each section is referenced in the `collections` list in `_config.yml`, and it has a matching template in the `_includes` directory that is imported in `index.html`, and a folder in the project root with a matching name prefaced with an underscore. Any files in the collection directory are rendered and included in the HTML when the project is built. You can control the order in which they render with a Frontmatter variable; there's an example of this on the work experience collection in the master branch.

If you don't need a section, remove it from the `collections` list in `_config.yml` and it won't show up in the menu or in the HTML. You can also remove the directory and files if you wish.

To add a section, add it to the collections list, create the directory and add entries, then use the Semantic UI docs and other examples here as inspiration for your template in the `_includes` directory. Lastly, add a reference to your include in `index.html`.

## Feedback

I'd love to hear what you think! Feel free to drop an issue here in the project or hit me up on [twitter](https://twitter.com/jameswrubel). Find a bug or have an idea for a change? Feel free to send a [pull request](https://help.github.com/articles/using-pull-requests/). I can't wait to see what you come up with!
