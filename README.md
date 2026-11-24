# BrokerCore presentation

**https://rahman-oxcel.github.io/brokercore-presentation/**

The page is AES-256 encrypted ([StatiCrypt](https://github.com/robinmoisson/staticrypt)).
Ask Rahman for the password. This repo is public, so only the encrypted output ships;
the source stays local in `src/` (git-ignored).

## Rebuilding

```
npx staticrypt src/journey.html -p "<password>" -d build --short --remember 30 --template-title "BrokerCore" --template-instructions "Enter the password to open the presentation." --template-placeholder "Password" --template-button "Open the presentation" --template-remember "Remember me on this device for 30 days" --template-error "That password didn't work." --template-color-primary "#001732" --template-color-secondary "#F5F6F8"
cp build/journey.html index.html
```

Keep `.staticrypt.json` (the salt) so a rebuild with the same password keeps "remember me" working.
