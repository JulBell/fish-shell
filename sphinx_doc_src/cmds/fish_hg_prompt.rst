.. _cmd-fish_hg_prompt:

fish_hg_prompt - output mercurial information for use in a prompt
=================================================================

Description
-----------

The fish_hg_prompt function can be used to display information about the current mercurial repository, if any.

For obvious reasons, it requires having hg installed.

There are numerous configuration options:

- $fish_color_hg_clean, $fish_color_hg_modified and $fish_color_hg_dirty: The color to use when the repo has the respective status

Some colors for status symbols:

- $fish_color_hg_added
- $fish_color_hg_renamed
- $fish_color_hg_copied
- $fish_color_hg_deleted
- $fish_color_hg_untracked
- $fish_color_hg_unmerged

And the status symbols themselves:

- $fish_prompt_hg_status_added, default '✚'
- $fish_prompt_hg_status_modified, default '*'
- $fish_prompt_hg_status_copied, default '⇒'
- $fish_prompt_hg_status_deleted, default '✖'
- $fish_prompt_hg_status_untracked, default '?'
- $fish_prompt_hg_status_unmerged, default '!'

And $fish_prompt_hg_status_order, which can be used to change the order the status symbols appear in. It defaults to ``added modified copied deleted untracked unmerged``.

See also fish_vcs_prompt, which will call all supported vcs-prompt functions, including git, hg and svn.

Example
-------

A simple prompt that displays hg info::

    function fish_prompt
        ...
        printf '%s %s$' $PWD (fish_hg_prompt)
    end


