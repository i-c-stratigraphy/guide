# Website publication

Pushes to master publish the themed Guide at https://stratigraphy.org/guide/ using GitHub Actions.
The workflow also builds the frozen original revision cab21a4e8f6f47e8160a03984e5d1423fb66d20b under /guide/old/.
Keep Settings → Pages configured for GitHub Actions; branch publishing would remove the archive.

Shared ICS includes, navigation, images and SCSS match the main website's Bulma Clean Theme.
The guide layout retains chapter navigation, and all chapter permalinks remain unchanged.

The legacy build uses the maintained Ruby dependencies and custom original layout.
The assembly script rebases local archive URLs and verifies that current files are unchanged.
Pull requests build and validate without deploying. Run the archive tests with:

    ruby scripts/test_assemble_sites.rb
