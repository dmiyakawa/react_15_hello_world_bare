# これはなに

React 15系（15.6.2）を使用したReact Hello WorldのHTML。

昔の本はここからスタートすることがあるのだが、今（2018-06-23）は create-react-app でnpm等もりもりで実装を開始するのであまり需要はない。あくまで参考用途で作成してみた

確認環境

 * 2018-06-23
 * macOS High Sierra 10.13.5
 * Chrome 67.0.3396.87


## React v16移行では動かない？何故？

JSXが基本的に当たり前であるという前提を理解しつつ最小のHello Worldを2018-06時点で作ってみようとしたところ16.4.1で動作しない。調べてみると factories がdeprecatedとなり、v16で削除されたとのこと。

バージョンを15.6.2に落としたところ、以下のような警告が出てくることを確認した（本サンプルでも出る）。

    Warning: Accessing factories like React.DOM.h1 has been deprecated and will be removed in v16.0+. Use the react-dom-factories package instead.  Version 1.0 provides a drop-in replacement. For more info, see https://fb.me/react-dom-factories

この警告は React 15.6.2 では少なくともconsole上に表示されるが、React 15.4 くらいでは出てこない。古い（といっても2017年3月とかだが）本ではカバーされておらず冒頭からしくじるという面白い（比喩）状況になる。

ちなみに、以前はreact.js, react-dom.jsを本家で配布していたようだが現在は直接配布していない。

## これからは？

変化が早い（というよりは独裁者のわがままのままに変化する）ライブラリということで、その都度最新のTutorialを見るのが正解。

現時点では create-react-app からいきなりFATなアプローチからの開始を期待される。
