# Nordic Love Data Week 2026

A public-facing website for the Nordic Love Data Week event (9–13 February 2026), built with [Jekyll](https://jekyllrb.com/) and hosted on [GitHub Pages](https://pages.github.com/).

**Live site:** https://dinghe.github.io/love-data-week-2026

## About the Event

Love Data Week is an international celebration of data, taking place every year during the week of Valentine's day. This year, for the first time, Nordic Love Data Week is organized by a consortium of Nordic universities, aiming to promote awareness and best practices in research data management, data sharing, and data literacy across the Nordic region.

**Event dates:** 9–13 February 2026  
**Registration opens:** 12 January 2026  
**Registration closes:** 9 February 2026

For more information about international activities, visit the [ICPSR event website](https://www.icpsr.umich.edu/sites/icpsr/about/news-events/international-love-data-week).

## Getting Started

### Prerequisites

This website is built with Jekyll, which requires [Ruby](https://www.ruby-lang.org). 

1. **Check if Ruby is installed:**
   ```bash
   ruby -v
   ```

2. **Install Ruby (if needed):**
   - **macOS (Apple Silicon M1/M2/M3):** Use Homebrew
     ```bash
     brew install ruby
     export PATH="/opt/homebrew/opt/ruby/bin:$PATH"  # Add to ~/.zshrc
     ```
   - **macOS (Intel):** 
     ```bash
     brew install ruby
     export PATH="/usr/local/opt/ruby/bin:$PATH"  # Add to ~/.zshrc
     ```
   - **Linux:** Follow the [Ruby installation docs](https://www.ruby-lang.org/en/documentation/installation/)
   - **Windows:** Install [RubyInstaller](https://rubyinstaller.org/) or use [Windows Subsystem for Linux](https://docs.microsoft.com/en-us/windows/wsl/)

### Local Development Setup

1. **Clone the repository:**
   ```bash
   git clone https://github.com/dinhe878/love-data-week-2026.git
   cd love-data-week-2026
   ```

2. **Create a Python virtual environment (optional, for data-related scripts):**
   ```bash
   python3 -m venv .venv
   source .venv/bin/activate  # On Windows: .venv\Scripts\activate
   ```

3. **Install Bundler:**
   ```bash
   gem install bundler
   ```

4. **Install Jekyll and dependencies:**
   ```bash
   bundle install
   ```
   
   If you encounter permission errors, delete the lockfile and regenerate it:
   ```bash
   rm Gemfile.lock
   bundle install
   ```

5. **Run the local development server:**
   ```bash
   bundle exec jekyll serve
   ```
   
   Then visit: [http://127.0.0.1:4000](http://127.0.0.1:4000)

6. **Auto-reload on config changes:**
   If you modify `_config.yml`, you'll need to restart the server (Ctrl+C, then re-run `bundle exec jekyll serve`). For automatic reloading, install guard:
   ```bash
   bundle add guard guard-jekyll-plus
   bundle exec guard init jekyll
   bundle exec guard
   ```

## Editing the Website

This is a Jekyll website using [Kramdown](https://kramdown.gettalong.org/quickref.html) Markdown and [Liquid](https://shopify.github.io/liquid/) templates.

### Key Configuration File: `_config.yml`

Main settings to update:

- **`title`** - Site title used in title bar and various places
- **`nav_title`** - Site name and strapline in the top navigation
- **`event_date`** - Event dates (displayed throughout the site)
- **`registration_opens_date`** / **`registration_closes_date`** - Registration period dates
- **`author`** - Primary contact/organizing institution
- **`mailbox_address`** - Contact email address (recommended: shared mailbox)
- **`description`** - Short event description (used by search engines and social media)
- **`url`** - Published site URL (without trailing slash)
- **`github_repo`** - GitHub repository name
- **`event_status`** - Controls page visibility based on event timeline (`soon`, `now`, `over`, `demo`)
- **`registration_status`** - Controls registration form visibility (`soon`, `open`, `closed`, `demo`)
- **`team`** - Team members with names, emails, images, affiliations, and social links

### Content Pages

Key pages to customize:

- **`index.md`** - Homepage/landing page
- **`agenda.md`** - Event schedule
- **`registration.md`** - Registration form and information
- **`projects.md`** - Hackathon/project listings
- **`activities.md`** - Links to helpful activities
- **`about.md`** - Information about the event and organizing team
- **`videos-slides.md`** - Event recordings and presentation slides
- **`code-of-conduct.md`** - Event code of conduct
- **`faq.md`** - Frequently asked questions

### Assets

- **`assets/logo.png`** - Logo displayed in the top navigation bar
- **`assets/advert.png`** - Image used when sharing on social media
- **Team member images** - Store profile photos in `assets/` (referenced in `_config.yml`)

### Adding Team Members

Edit the `team` list in `_config.yml`:

```yaml
team:
  - name: Team Member Name
    email: email@example.com
    image: /assets/member-photo.jpg
    affiliation: University Name
    title: Position/Role
    links:
      - title: Website
        url: https://example.com
        icon: bi-globe2
      - title: GitHub
        url: https://github.com/username
        icon: bi-github
```

Team members are automatically displayed on the `about.md` page.

### Adding Navigation Pages

1. Create a new Markdown file in the repository root
2. Add front matter with `menu_title` and `menu_icon` (Bootstrap Icons):
   ```markdown
   ---
   title: Page Title
   menu_title: Nav Label
   menu_icon: icon-name
   ---
   ```
3. Add the filename to `header_pages` in `_config.yml`

### Useful Liquid Tags

- **Reference config variables:** `{{ site.event_date }}`
- **Link to pages:** `[Link text]({{ site.baseurl }}{% link page-name.md %})`
- **Loop through team members:** 
  ```liquid
  {% for member in site.team %}
    {{ member.name }} - {{ member.affiliation }}
  {% endfor %}
  ```

See [Jekyll Liquid documentation](https://jekyllrb.com/docs/liquid/) for more.

## Publishing Changes

After making changes locally and testing:

```bash
git add .
git commit -m "Describe your changes"
git push
```

The site will automatically rebuild and deploy to GitHub Pages (usually within a few minutes). Force-refresh your browser to see changes.

## Project Structure

```
.
├── _config.yml              # Main configuration file
├── _includes/               # Reusable page components
│   ├── header.html
│   ├── footer.html
│   ├── breadcrumbs.html
│   └── youtube.html
├── _layouts/                # Page templates
│   ├── default.html
│   ├── project.html
│   └── notebook.html
├── _projects/               # Individual project pages
│   ├── 01-project-title.md
│   └── 02-project-title.md
├── assets/                  # Images and stylesheets
│   ├── main.scss
│   ├── logo.png
│   └── advert.png
├── activities/              # Event activities and templates
│   ├── environment/         # Python environment files
│   └── templates/           # Email and form templates
├── Gemfile                  # Ruby dependencies
└── *.md                     # Main content pages (index, agenda, etc.)
```

## Contributing

To contribute to this website:

1. Create a branch for your changes
2. Make edits and test locally
3. Commit and push your changes
4. Submit a pull request

## Acknowledgements

This website template is based on the [Hackathon Website Template](https://github.com/JGIBristol/hackathon-template) developed by the [Jean Golding Institute](https://www.bristol.ac.uk/golding/) at the University of Bristol, specifically by [James Thomas](https://github.com/jatonline).

The template was originally created for the [CMIP6 Data Hackathon](https://cmip6moap.github.io/) (2–4 June 2021) and has been adapted for use by the Nordic Love Data Week 2026 organizing consortium.

## License

See the [LICENSE](LICENSE) file for details.

## Contact

For questions about the Nordic Love Data Week, please contact:  
**{{ site.author }}** - [{{ site.mailbox_address }}](mailto:{{ site.mailbox_address }})

