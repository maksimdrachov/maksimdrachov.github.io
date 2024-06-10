Serve on `http://localhost:4000/`
```
bundle exec jekyll serve
```

Build website & push to github
```
bundle exec jekyll build
rm -rf _docs
mv _site ./docs # Github Pages serves from here!
git add .
git commit -m "..."
git push
```

Website:
[maksimdrachov.github.io](https://maksimdrachov.github.io/)
