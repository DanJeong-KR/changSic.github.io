---
layout: post
title:  "What are Design Patterns?"
date:   2019-11-09
excerpt: ""
tag:
- iOS
- DesignPattern
comments: true
---
* What are Design Patterns?
  * [A real-world example](#ex)
  * [Example explanation](#ex_detail)
  * [Types of design patterns](#type)
  * [Criticisms of design patterns](#criticisms)
  * [Benefits of design patterns](#benefits)
  * [Key Points](#key)
* How to Read a Class Diagram.

이 글은 raywenderlich에서 발행한 Design Patterns By Tutorials 의 Chapter 1. What are Design Patterns? 을 번역한 것으로 출처를 밝힙니다!

## <a id="ex">A real-world example</a>
The introduction told you that design patterns are reusable, template solutions to common development problems.

디자인 패턴은 개발에서 발생하는 일반적인 문제에 대한 재사용 가능하고 템플릿한 해결책 입니다.

Design patterns aren’t concrete implementations, but rather, serve as starting points for writing code.

디자인 패턴은 구체적으로 어떤 것을 실행하는 것이기 보다 코드 작성을 시작하는 시점의 역할을 합니다.

They describe generic solutions to problems that experienced developers have encountered many times before.

그것들은 개발자들이 이전에 무수히 마주했던 문제에 대한 포괄적인 해결책을 설명합니다.

What does this mean exactly...? Consider this non-development, real-world scenario:

이것이 무엇을 의미할까요? 개발이 아닌 현실세계의 시나리오로 생각해봅시다.

You’re the proud owner of a gardening company, and your business is really, er, blooming.

당신은 가든 회사의 대표이며 사업은 정말로 번창중이라고 합시다.

You’ve only done a few small projects up to now - a tree planted here, and maybe a few flowers there.

당신은 지금까지 작은 프로젝트만을 완료했다. 여기 나무를 심고 아마 약간의 꽃들도

However, you just landed a big client who wants several dozen trees and flowers planted on their property.

하지만 수십그루의 나무와 꽃이 자신의 부동산에 심어져 있길 바라는 클라이언트를 만났습니다.

Your standard procedure has been for your employees to carry each flower or tree sapling into place individually.

당신의 일반적인 과정은 직원들이 각각의 꽃과 나무 샘플을 개별적으로 옮기는 작업입니다.

Once the flower has been temporarily placed in the flowerbed, your customer inspects and approves the arrangement before you plant everything in the ground.

일단 꽃이 일시적으로 화단에 옮겨지면 당신의 고객은 그것을 검사하고 식물이 땅에 모두 심어지기 전에 협의합니다.

You’re worried it’s going to take forever to carry each flower and tree into place for this large project.

당신은 이 큰 프로젝트를 위해 꽃과 나무를 옮기는데 너무 오래 걸릴 것을 걱정합니다.

And you even need a few people to carry some of the bigger trees.
심지어 몇개의 큰 나무를 옮길 사람들도 필요합니다.

While you could hire lots of temporary employees, you wouldn’t make a profit on the job. There’s got to be a better way!

많은 임시직을 고용할 순 있지만 그 job에서 이득을 얻진 못할 것입니다. 더 좋은 방법이 있을 것입니다!

You decide to ask other gardeners what they do, and you find out they use wheelbarrows and carts.

당신으 다른 정원사에게 그들은 무얼하는지 물어봅니다. 그리고 손수레와 카트를 사용하는 것을 찾아냅니다.

what a great idea!
You tell your employees to use a cart to move multiple flowers at the same time into place and a wheelbarrow to move the heavy trees.

당신은 직원들에게 한번에 여러 꽃들을 카트를 사용해서 옮기고 큰 나무는 손수레를 사용하라고 합니다.

In the meantime, you use a lounge chair chair to watch your workers go to it... isn’t management great?

그 동안에 당신은 직원들이 잘 하는지 보려고 의자를 사용합니다. 이 관리는 좋지 않나요?

So now you know all about design patterns! Wait, you need more details? Okay, let’s break it down...

당신은 디자인 패턴에 대해 다 배운 거에요. 자세히 알고 싶나요? 하나씩 봅시다.

## <a id="ex_detail">Example explanation</a>
The “design pattern” here is the use of wheelbarrows and carts.

여기에서 '디자인 패턴'은 손수레와 카트를 사용하는 것입니다.

These are common, best practice tools in gardening.

이런 것들은 일반적이며 gardening을 하는 좋은 모범 툴입니다.

Similarly, software design patterns form a set of best practices in development.

유사하게도, 소프트웨어 디자인 패턴은 개발영역에서 모범 사례의 집합을 만드는 것입니다.

You could have chosen not to use wheelbarrows and carts, but akin to avoiding software design patterns, you assume more risk by making the project more time- and labor-intensive.

당신은 손수레와 카트를 사용하지 않기로 했을 수도 있지만 소프트웨어 디자인 패턴을 회피하는데 유사하게도 당신은 프로젝트를 보다 시간과 노동 집약적으로 만듬으로써 더 큰 위험을 감수해야 할 것으로 추정해야 한다.

Back to the point of “asking other gardeners what they do.”

다른 정원사에게 그들으 하는 것을 물어보는 시점으로 돌아가서

Most design patterns have been around for a long time — having started life in the 1970s and 1980s — and they continue to work well to this day.

대부분의 디자인 패턴들은 오랜시간 존재해왔으며 (1970 ~ 1980년대 부터 시작되어 왔다) 요즘에도 잘 동작하며 이어지고 있다.

This longevity is partly due to the fact their use has been validated in many projects over the decades, but it’s also because they aren’t concrete solutions.

이러한 장수는 특히 디자인패턴을 사용하는 것이 수십년간 많은 프로젝트에서 효과적이었다는 사실 때문이며 또한 디자인패턴이 문제의 구체적인 해결책이 아니라는 것 때문이기도 하다.

In the gardening scenario, you decided that carts will be used to move flowers and wheelbarrows will be used to move trees.

정원 시나리오에서 카트는 꽃을, 손수레는 나무를 옮기는 데 사용될 것이라고 결정했다.

These are implementation details: you could have used carts to move both flowers and trees, only used wheelbarrows, or any other combination that made the job easier.

이것들은 디테일한 실행이다. 당신은 카트를 꽃과 나무 모두를 옮기는 데 사용할 수도 있었다. 아니면 손수레만을 사용하든, 또한 일을 더 쉽게 만드는 다른 조합을 사용할 수도

Design patterns are generic, go-to solutions for solving common problems, like using wheelbarrows and carts.

디자인 패턴은 손수레와 카트를 사용한것과 같이 포괄적이며 일반적인 문제를 해결하기 위한 go-to solution 이다.

They are starting points for concrete implementations, like using carts for flowers and wheelbarrows for trees.

디자인 패턴은 꽃은 카트를 사용하고 나무는 손수레를 사용하는 것과 같은 구체적인 실행방법들의 시작점이다.

Make sense? Great! It's now time to leave the garden behind and head back to the world of software design patterns.

## <a id="type">Types of design patterns</a>

There are three main types of design patterns:
1. Structural design pattern: Describes how objects are composed and combined to form larger structures.

구조적 디자인 패턴 : 객체들이 어떻게 큰 구조를 이루기 위해 구성되고 결합되는지를 설명한다.

Examples of structural design patterns include Model-View- Controller (MVC), Model-View-ViewModel (MVVM) and Facade.

구조적 디자인 패턴의 예로 MVC, MVVM, Facade 가 있다.

2. Behavioral design pattern: Describes how objects communicate with each other.

행위적 디자인 패턴 : 객체들이 어떻게 서로 소통하는지를 설명한다.

Examples of behavioral design patterns are Delegation, Strategy and Observer.

행위적 디자인 패턴의 예로는 Delegation, Strategy, Observer 가 있다.

3. Creational design pattern: Describes how to create or instantiate objects.

창조적 디자인 패턴 : 객체를 인스턴스화 하거나 창조하는 방법을 설명한다.

Examples of creational patterns are Builder, Singleton and Prototype.

창조적 디자인 패턴의 예로는 Builder, Singleton, Prototype 이 있다.

You may be wondering if knowing a design pattern’s type really matters. Well, yes...and no.

당신은 디자인 패턴의 타입을 하는 것이 정말로 중요한지 궁금해 할 수도 있다. 음.. 맞고도 아니야.

It’s not useful to memorize all patterns by type. Most developers don’t do this.

타입별로 모든 패턴을 기억하는 것은 유용하지 않아. 대부분의 개발자들이 이렇게 하지도 않고

However, if you’re not sure whether a particular pattern will work, it’s sometimes useful to consider other patterns of the same type.

하지만 만약 당신이 특정 패턴이 잘 동작할지 않할지 확신하지 못할 때 같은 타입의 다른 디자인 패턴을 고려하는 게 가끔씩 유용할 때가 있어.

You just might find one that works better for your particular problem.

당신은 당신이 가지고 있는 특정 문제에 잘 작동하는 것을 바로 찾을 수도 있지!

Note: There’s an ongoing debate on whether some patterns, including MVVM and MVC, are actually architectural patterns, which span an entire app or subsystem architecture.

MVVM이나 MVC 같은 패턴은 실제로는 전체 앱 혹은 하위 시스템 아키텍처로 포괄하는 아키텍처 패턴인 것인지 아닌지에 대한 논쟁은 계속 이어지고 있다.

Hence, they are broader in scope than design patterns, which only span components or pieces of an app.

이러한 이유로 그것들은 구성요소들 혹은 앱의 조각으로 포괄되는 디자인 패턴 보다는 더 넓은 스코프를 가지고 있다.

Architectural patterns can even use or encompass several design patterns.

아키텍처 패턴은 심지어 몇몇 디자인 패턴을 사용하거나 포함시킬 수 있어. (더 큰 개념이라는 뜻)

For the purposes of this book, a comprehensive discussion of architectural patterns is out of scope.

이 책의 목적은 아키텍처 패턴의 논의는 논외로 합니다.

We’ve chosen to label MVVM and MVC as structural design patterns because they can be used alongside other design patterns in a component fashion.

우리는 MVVM 과 MVC를 구조적 디자인 패턴으로 명시했습니다. 왜냐하면 이것들은 어떤 구성 방식의 관점에서 다른 디자인 패턴을 동시에 사용될 수 있기 때문입니다.

They are also very commonly used in iOS projects, and we wanted to ensure we covered them.

그것들은 또한 매우 일반적으로 iOS 프로젝트에 사용되고 우리는 그것들을 다룰 수 있도록 하길 바랬습니다.

If someone says these are actually architectural patterns, we don’t necessarily disagree, as they can also be used that way.

누군가가 이것들이 실제로는 아키텍처 패턴이라고 한다면 그것들이 또한 그 방식으로 사용될 수 있기 때문에 우리는 꼭 disagree 하진 않을 것입니다.

## <a id="criticisms">Criticisms of design patterns</a>

As indicated earlier, “there are no silver bullets in software development,” and design patterns are no exception to this.

앞서 표현한 것과 같이 소프트웨어 개발에서 은화살은 없고 디자인 패턴도 예외는 아니다.

This means that simply knowing and employing design patterns will not guarantee you will create a well-architected piece of software.

이것은  간단하게 디자인 패턴을 아는 것과 그것을 채택하는 것이 잘 짜여진 소프트웨어의 조각을 만들 것이라는 것을 보증하지 않는다는 의미이다.

There are dozens of design patterns, so knowing when and how to employ each one is important.

많은 디자인 패턴들이 있고 각각을 언제 그리고 어떻게 채택할 것인지가 중요하다.

Here are some common criticisms of design patterns:

여기 일반적인 디자인 패턴의 비판이 있다.

* If you overuse design patterns, your project can become overly complex.
* 만약 당신이 디자인 패턴을 과하게 사용한다면, 프로젝트는 매우 복잡해질 수  있다.
You need to be careful about overusing any tool, including design patterns.

당신은 디자인 패턴을 포함한 어떤 툴이든 과하게 사용하는 것에 대해 조심할 필요성이 있다.

You can minimize this issue by clearly and correctly defining the problem to be solved before adding a design pattern to your project.

당신은 이 문제를 디자인 패턴이 당신의 프로젝트에 추가되기 전에 해결될 수 있다는 것을 명확하고 정확하게 정의함으로써 최소화할 수 있다.

* Many design patterns are made redundant by modern programming languages.
* 많은 디자인 패턴들은 현대 프로그래밍 언어에 의해 불필요해지게 되었다.

It’s true that modern programming languages like Swift make some design patterns irrelevant or trivial to implement.

스위프트 같은 현대 프로그래밍 언어가 몇몇 디자인 패턴들 상관없게 혹은 사소하게 만든 것은 사실이다.
However, just because some patterns are provided via a programming language doesn’t mean all patterns will be.

하지만 단지 몇몇 패턴이 프로그래밍 언어로 제공된다는 것이 모든 패턴이 그렇다는 것을 의미하는 것은 아니다.

* Design patterns are a lazy substitute for learning object-oriented
principles.
* 디자인 패턴은 객체 지향적인 원칙들을 배우는 것에 대한 게으른 대체제이다.

Why not learn both? A strong understanding of object-oriented principles will certainly help you in your development.

왜 둘 다 배우지 않아? 객체 지향의 원칙들의 높은 이해는 당신의 개발에서 확실히 도움이 될 거야.

However, if you already know a design pattern works well for a particular problem, why should you reinvent the solution from scratch?

하지만, 만약 당신이 이미 특정 문제에 대해 디자인 패턴이 잘 작동한다는 것을 알고 있다면 왜 해결책을 처음부터 다시 개발해야 하지?

* But, but...check out this thread on Twitter, which definitely shows that design patterns are worthless!
* 근데 트위터에서 이 쓰레드를 확인해봐, 그게 디자인 패턴의 무가치함을 확실하게 보여줄거야.

Regardless of the particular criticism, design patterns have been around for a long time, and they’ve been used in many apps.

어떤 비난에도 불구하고 디자인 패턴은 오랜시간 있어왔고 많은 어플에서 사용되고 있어.

So at some point, you’re going to encounter them.

그래서 몇몇 관점에서는 당신은 그것들을 마주하게 될거야.

We think it’s best to have an understanding of what they are before you run into them, instead of trying to wing it on the fly, which in our experience is usually late on a Sunday night, the day before the release deadline, right after discovering a critical bug.

우리는 그것을 하늘에서 날개를 피려고 노력하는 것 대신에 run into 하기 전에 그게 무엇인지 이해하는 것이 좋다고 생각해. 그것은 내 경험에서는는 보통 데드라인 하루 전 늦을 일요일 밤 치명적인 버그를 발견한 바로 직후야.
(모르고 가서 개 고생하기 전에 미리 아는것이 좋다고 표현한 듯.)

## <a id="benefits">Benefits of design patterns</a>

We’ve mentioned many benefits of design patterns already, but we wanted to point out a few more:

우리는 이미 디자인 패턴의 많은 장점들을 언급했지만 조금 더 집고 넘어갈게

* Design patterns create a common language.
* 디자인 패턴은 보통의 언어를 만든다.

Instead of describing a particular solution in detail, you can simply state which design pattern you think would work best.

특정 솔루션을 자세하게 설명하는 대신에, 넌 간단하게 너가 생각한 디자인 패턴이 잘 작동할 것이라고 명시할 수 있어.

This streamlines communication between developers.

이것은 개발자들 사이의 의사소통을 간소화합니다.

* Design patterns fast-track developer onboarding.
* 디자인 패턴은 빠른 개발자 온보딩이다. (온보딩 : 새로 합류한 사람이 빠르게 조직의 문화를 익히고 적응하도록 돕는 과정 같은거.)

It’s much easier to onboard a new developer on a project that uses design patterns, than on a project with completely custom logic.

완전하게 커스텀 로직으로 구성된 프로젝트 보다 디자인 패턴을 사용하는 프로젝트에서 새로운 개발자가 더 적응하기 쉽다.

* Design patterns make you a better person.
* 디자인 패턴은 당신을 더 나은 사람으로 만듭니다.

Well, this one may still be up for debate. But some degree of self-improvement is never wasted!

음, 이건 아마 여전이 논쟁의 여지가 있지만 어느 정도의 자기개발은 결코 낭비가 아니에요!

However, there is a grain of truth to this, as the next developer to maintain your project will certainly think you’re a better person for having left them a nice, design- pattern-filled project instead of a spaghetti-coded mess!

하지만, 이 진실의 일면에는 당신의 프로젝트를 유지보수하는 다음 개발자가 확실히 당신을 좋은 사람으로 생각할 것이기 때문에 spaghetti-coded mess 대신에 디자인 패턴이 채워진 프로젝트가 좋다.

* Knowing design patterns allow you to spot similarities between code.
* 디자인 패턴을 아는 것은 너가 코드 사이의 유사점을 찾게 해준다.

Once you know and understand different design patterns, you begin to notice their use in code.

한번 당신이 다른 디자인 패턴들을 알고 이해한다면, 넌 코드에서 그것들의 사용을 알아차리기 시작할 것이다.

This gives you a leg up as you are at least a little familiar with how to use that code.

이는 적어도 너가 그 코드를 사용하는 방법에 대해 약간 익숙하기 떄문에 널 도와준다.

For example, iOS and Mac programming makes heavy use of the Delegation pattern.

예를 들어, iOS 와 Mac 프로그래밍은 Delegation Pattern 을 매우 많이 사용한다.
You would spot this pattern easily if you ever moved to another platform that also uses Delegation and instantly be familiar with how the code is organized.

넌 만약 너가 Delegation 을 많이 사용하는 다른 플랫폼으로 옮겨가더라도 이 패턴을 쉽게 발견할 거고 바로 어떻게 코드가 구성되 있는지 익숙하게 될 것이다.


## <a id="key">Key Points</a>

In this chapter, you learned what design patterns are and why you should care about them. Here are the key points to remember:

* Design patterns aren't concrete implementations, but rather, they are a starting point for writing code.

디자인 패턴은 구체적으로 실행하는 것이 아니라 오히려 코드를 작성하는 시작점에 가깝다.

* Design patterns collectively form a set of best practices to help you write more understandable and easier-to-maintain code.

디자인 패턴은 집합적으로는 너가 더 이해학 쉽고 유지보수하기 쉬운 코드를 작성하는데 도움이 되는 좋은 방식들의 집합을 형성하게 한다.

* There are three main types of design patterns: structural, behavioral and creational.

디지인 패턴에는 3개의 타입이 존재한다. structural, behavioral, creational

* There are both criticisms and benefits of design patterns.

디자인 패턴에는 비판적인 부분과 긍정적인 부분 모두 존재한다.

Ultimately, they are commonplace in software development, and you're likely to encounter them. Therefore, having a good grasp of them is important.

궁극적으로 디자인 패턴은 소프트웨어 개발에서 매우 흔하고 넌 그것들을 계속 마주하게 될 거야. 그러므로 디자인 패턴을 잘 이해하는 것이 중요하지.
