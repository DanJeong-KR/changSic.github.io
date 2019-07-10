---
layout: post
title:  "Github Commit Message 규칙 만들기"
date:   2019-07-10
excerpt: "Commit meesage 작성시 원칙을 정하고 일관성을 유지해서 프로젝트 관리를 더 체계적으로 해보자.
"
tag:
- iOS
- Git
comments: true
---

<h1 id="git---commit-message-convention" md-pos="2-33"><a href="#git---commit-message-convention" name="git---commit-message-convention" class="anchor"><span class="octicon octicon-link"></span></a>Git - Commit Message Convention</h1>
<h2 id="1-commit-message-structure" md-pos="114-141"><a href="#1-commit-message-structure" name="1-commit-message-structure" class="anchor"><span class="octicon octicon-link"></span></a>Commit Message Structure</h2>

기본적으로 커밋 메세지는
* Subject (제목)
* Body (본문)
* Footer (꼬리말)

로 구성한다.

<pre md-pos="182-219" class="line-numbers"><code md-pos="186-215">type : subject

body

footer
</code></pre>
<h2 id="2-commit-type" md-pos="223-237"><a href="#2-commit-type" name="2-commit-type" class="anchor"><span class="octicon octicon-link"></span></a>1. Commit Type</h2>

* `feat` : 새로운 기능 추가
* `fix` : 버그 수정
* `docs` : 문서 수정
* `style` : 파일 그룹화, 세미콜론 누락, 코드 변경이 없는 경우
* `refactor` : 코드 리펙토링
* `test` : 테스트 코드, 리펙토링 테스트 코드 추가
* `chore` : 빌드 업무 수정, 패키지 매니저 수정


<h2 id="3-subject" md-pos="414-424"><a href="#3-subject" name="3-subject" class="anchor"><span class="octicon octicon-link"></span></a>2. Subject</h2>
<ul>
  <li md-pos="426-469">제목은 50자를 넘기지 않고, 대문자로 작성하고 마침표를 붙이지 않는다.</li>
  <li md-pos="469-540">과거시제를 사용하지 않고 명령어로 작성한다.
    <ul>
      <li md-pos="498-518">&quot;Fixed&quot; --&gt; &quot;Fix&quot;</li>
      <li md-pos="520-540">&quot;Added&quot; --&gt; &quot;Add&quot;</li>
    </ul>
  </li>
</ul>
<h2 id="4-body" md-pos="544-551"><a href="#4-body" name="4-body" class="anchor"><span class="octicon octicon-link"></span></a>3. Body</h2>
<ul>
  <li md-pos="553-591">선택사항이기 때문에 모든 커밋에 본문내용을 작성할 필요는 없다.</li>
  <li md-pos="591-627">부연설명이 필요하거나 커밋의 이유를 설명할 경우 작성해준다.</li>
  <li md-pos="627-666">72자를 넘기지 않고 제목과 구분되기 위해 한칸을 띄워 작성한다.</li>
</ul>
<h2 id="5-footer" md-pos="670-679"><a href="#5-footer" name="5-footer" class="anchor"><span class="octicon octicon-link"></span></a>4. footer</h2>
<ul>
  <li md-pos="681-718">선택사항이기 때문에 모든 커밋에 꼬리말을 작성할 필요는 없다.</li>
  <li md-pos="718-750">issue tracker id를 작성할 때 사용한다.</li>
</ul>
<h2 id="6-example" md-pos="754-764"><a href="#6-example" name="6-example" class="anchor"><span class="octicon octicon-link"></span></a>5. Example</h2>
<pre md-pos="766-1804" class="line-numbers"><code md-pos="770-1800">feat: Summarize changes in around 50 characters or less

More detailed explanatory text, if necessary. Wrap it to about 72
characters or so. In some contexts, the first line is treated as the
subject of the commit and the rest of the text as the body. The
blank line separating the summary from the body is critical (unless
you omit the body entirely); various tools like `log`, `shortlog`
and `rebase` can get confused if you run the two together.

Explain the problem that this commit is solving. Focus on why you
are making this change as opposed to how (the code explains that).
Are there side effects or other unintuitive consequenses of this
change? Here's the place to explain them.

Further paragraphs come after blank lines.

 - Bullet points are okay, too

 - Typically a hyphen or asterisk is used for the bullet, preceded
   by a single space, with blank lines in between, but conventions
   vary here

If you use an issue tracker, put references to them at the bottom,
like this:

Resolves: #123
See also: #456, #789
</code>
</pre>


<h2 id="8-references" md-pos="2332-2345"><a href="#8-references" name="8-references" class="anchor"><span class="octicon octicon-link"></span></a>References</h2>
<ul>
  <li md-pos="2347-2406"><a href="http://sujinlee.me/professional-github/" md-pos="2349-2405">깃허브로 취업하기 포스팅</a></li>
  <li md-pos="2406-2473"><a href="https://udacity.github.io/git-styleguide/" md-pos="2408-2472">유다시티 커밋 메시지 스타일 가이드</a></li>
</ul>
</article>
