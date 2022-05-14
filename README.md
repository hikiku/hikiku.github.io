# hikiku.github.io

## Setup Project

[Instructions](https://jekyllrb.com/docs/#instructions)

```bash
# Check your Jekyll version
jekyll -v
# jekyll 4.2.2

# install the jekyll and bundler gems.
gem install jekyll bundler

# Create a new Jekyll site
jekyll new hikiku.github.io
cd hikiku.github.io

# If you are using Ruby version 3.0.0 or higher, step 5 may fail. You may fix it by adding webrick to your dependencies:
bundle add webrick

# Build the site and make it available on a local server.
bundle exec jekyll serve

# Browse to http://localhost:4000
```

