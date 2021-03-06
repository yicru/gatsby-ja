---
title: MDX で Markdown にコンポーネントを追加する
---

Markdown を使って長いコンテンツを作るとき、[コンポーネント](/docs/glossary/#component)を埋め込みたくなるかもしれません。これは多くの場合、コンテンツを JSX で書くか、カスタム文法を使うプラグインを利用することで解決されます。1 つ目の手段の JSX はコンテンツを書くのに優れたフォーマットではなく、コンテンツがチームにとって親しみづらくなってしまうため、最適ではありません。カスタム文法とプラグインを使う方法はとても柔軟性に欠ける場合が多く、構造化を促進しません。もしあなたが自分のコンテンツにコンポーネントを追加したいなら、 MDX をプロジェクトに追加する Gatsby プラグインである `gatsby-plugin-mdx` を使うことをおすすめします。

## MDX とは？

[MDX][mdx] はコンポーネント時代のための Markdown です。MDX では、 Markdown の中に JSX を埋め込むことができます。これは文章を Markdown の簡潔な文法を使って（たとえば `# 見出し` のように）書くことができ、より高度なことをしたり、コンポーネントを再利用したりするのには JSX を使える、素晴らしい組み合わせです。

MDX は、文章が主体なサイトに、図表やアラートなどのコンポーネントを、プラグインの設定なしで追加するのに役立ちます。それは「設定より構成」を強調し、ブログの記事やデザインシステムの文書化、没入型あるいは動的なインタラクションのある長い記事で真価を発揮します。

MDX では、MDX ドキュメントをインポートし、コンポーネントとして利用できます。これにより、一箇所に用意した FAQ ページなどを、ウェブサイトの全体で再利用できます。

## 実際にどうなるのか

インポートと JSX 文法は、コンポーネント内で使うのと同じようにはたらきます。これによって、開発者とコンテンツ製作者の間でシームレスな体験を得られます。Markdown と JSX は以下のように一緒に使うことができます。

```markdown
import { Chart } from '../components/chart'

# チャートです

このチャートは MDX ドキュメント中で描画されます。

<Chart />
```

## 特長

❤️ **パワフル**: MDX は Markdown と JSX の文法を React/JSX に完璧にフィットするよう融合させます。

💻 **すべてがコンポーネント**: すでにあるコンポーネントを MDX で使ったり、他の MDX ファイルを
プレーンなコンポーネントとして使ったりできます。

🔧 **カスタマイズ可能**: それぞれの Markdown 要素の描画に、どのコンポーネントを使うかを設定できます（`{ h1: MyHeading }`）。

📚 **Markdown ベース**: Markdown の簡単さ、単純さを保ちます。JSX を使うのは、あなたが使いたいと思ったときだけです。

🔥 **超高速**: MDX にランタイムはありません。すべての構築作業はビルド段階で行われます。

<GuideList slug={props.slug} />

[mdx]: https://mdxjs.com
