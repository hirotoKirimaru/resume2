# 職務経歴書

Wordで管理したり、いろんなサービスに登録して情報が散ってしまっているので、めんどくさいのでGitHubに集約させる。

# GitHub Pages

- 通常用
    - https://hirotokirimaru.github.io/resume2/
- 印刷用
    - https://hirotokirimaru.github.io/resume2/forPdfReadme



# 過去に職務経歴書を作ったもの

- https://job-draft.jp/user/dashboard
- https://jobs.forkwell.com/
- https://findy-code.io/home


# PDFの存在

Releasesを確認すること
- https://github.com/hirotoKirimaru/resume2/releases

---

## 作成元GitHub

https://github.com/kawamataryo/resume

## Features

### 💅 Lint text

Automatic proofreading with [textlint](https://github.com/textlint/textlint).

```
$ yarn lint --fix
```
It is also automatically executed when pre-commit by [husky](https://github.com/typicode/husky).  
proofreading rules are set with `.textlintrc`.



### 📝 Convert MD to PDF

You can generate PDF with [md-to-pdf](https://www.npmjs.com/package/md-to-pdf).


```
$ yarn build:pdf
```

The output PDF can be styled as you like with CSS. Edit the `pdf-configs/style.css`.  

### 🛠 Create release

When you push with a `v**` tag, GitHub Actions will run the build, generate the PDF, create a Release, and register the PDF to Assets.

```
$ git commit -m "add job"
$ git tag v1.0
$ git push origin --tags
```

### 📆 Remind update

Automatically generate issues every three months with GitHub Actions Schedules triggers to prompt you to update your resume.

To change the duration or stop the job, edit `.github/workflows/create-issue.yml`.  
To change the issue contents, edit `.github/ISSUE_TEMPLATE.md`.
