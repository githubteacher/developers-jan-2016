# GitHub for Developers

Jan 20-21, 2016
https://training.github.com/kit/courses/github-for-developers.html

## Resources

- [Survey](https://www.surveymonkey.com/r/PR7STH6)
- [Git Branching](http://pcottle.github.io/learnGitBranching/)
- [Git reference docs](http://git-scm.com/docs)
- [Git cheat sheet](http://training.github.com/kit/downloads/github-git-cheat-sheet.pdf)
- [*ProGit*](http://git-scm.com/book) by Scott Chacon (free)
	- [section on Git aliases](http://git-scm.com/book/en/v2/Git-Basics-Git-Aliases)
- [Git for Windows](https://msysgit.github.io/)
- [GitHub Guides](http://guides.github.com)
  - [Mastering Markdown](https://guides.github.com/features/mastering-markdown)
- [Fork and Pull Request help articles](https://help.github.com/articles/using-pull-requests/#fork--pull)
- [GitHub Training YouTube Channel](http://youtube.com/githubguides)
	- [Reset](https://www.youtube.com/watch?v=BKPjPMVB81g)
	- [Forking](https://www.youtube.com/watch?v=5oJHRbqEofs)
	- [Pull Requests](https://www.youtube.com/watch?v=d5wpJ5VimSU&list=PLg7s6cbtAD15G8lNyoaYDuKZSKyJrgwB-&index=19)
	- [Rebase](https://www.youtube.com/watch?v=SxzjZtJwOgo&list=PLg7s6cbtAD15G8lNyoaYDuKZSKyJrgwB-&index=22)
- GitHub Training's [review class schedule](http://training.github.com/schedule/) (regular, free webinars)
- [Overview](https://github.com/integrations) of third-party integrations

#### Show Current Branch in Terminal Prompt
Put this in your `.bashrc` or `.bash_profile`:

```bash
parse_git_branch() {
  git branch 2> /dev/null | sed -e '/^[^*]/d' -e 's/* \(.*\)/ (\1)/'
}
export PS1="\w\[\033[36m\]\$(parse_git_branch) \[\033[00m\] > "
```
