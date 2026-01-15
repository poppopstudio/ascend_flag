# Ascend flag

Recipe/module to enable flagging of resources functionality for Ascend.

## Installation

### Add the repository to composer

```composer
{
    "type": "vcs",
    "url": "git@github.com:poppopstudio/ascend_flag.git"
},
```

### Add the patch

Change directory into /patches and
`wget https://www.drupal.org/files/issues/2020-05-28/flagging_global-3143606-3.patch`

```composer
"drupal/flag": {
    "Missing 'global' in flag object - https://www.drupal.org/project/flag/issues/3143606": "patches/flagging_global-3143606-3.patch"
}
```

### Install the module and dependencies via the recipe

From project root, `drush recipe ../recipes/ascend_flag`

If this step gives you an error like `"flag" is not a known module or theme`
you will need to clear cache and reenter the recipe command.
