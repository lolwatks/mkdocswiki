---
description: Step-by-step guide on how you can use bot to link to existing FAQ entries
---

# How to link FAQ via bot in Discord

## Intro 🍁

As a community of investors, we get queries from time to time, that are frequently asked. Often repeatedly.

We have FAQs on our wiki, for queries such as these, that addresses such queries. But having it in an archive is of no value, if it cannot be searched and linked, as and when needed.

We've a setup that solves this problem - any active member can invoke the bot with a specific tag, and the bot would take care of presenting right information to the user.

![Sample invocation of bot against a common query - Dark mode](/images/sample-bot-invoke.dark.png)

![Sample invocation of bot against a common query - Light mode](/images/sample-bot-invoke.light.png)

We'll explore next how to invoke this bot

## List of tags 📚

We use Carl-bot's tag feature at present to achieve this.

Every time a new FAQ entry is created, it gets a corresponding `tag` entry for Carl bot.

List of all available tag-based triggers can be found by typing `.taglist` in `#test` channel in our Discord.

Once this message is typed, Carl-bot would DM you the list of available tags.

![Sample message sent by bot - Dark Mode](/images/bot-dm-taglist.dark.png)

![Sample message sent by bot - Light mode](/images/bot-dm-taglist.light.png)

Above image(s) are illustrative. Actual list can be different, and change from time to time. For latest updated list, you can use `.taglist` in `#test` channel.

## Table of tags 🏓

Below are the exhaustive list of all tags, what kind of typical query / comment should someone ask to get that as response, and the expected response from bot .

| Trigger words   | Typical comment                                                                                               | Expected response                                                                                                                                                                                                                                                                                                                                                            |
|:----------------|:--------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `.disc`         | *What should I know before I start reading the wiki?*                                                         | Hey `@user`, before you start reading our wiki, it's best you read through our disclaimers and disclosures. Just because we discuss a specific stock, or bond, or mutual fund, or even any investment apps in our wiki; doesn't mean we're recommending those. [Read more here](https://indiainvestments.gitbook.io/content/disclaimers-and-disclosures)                     |
| `.direct`       | *Why should I invest in direct plans?*                                                                        | Hey `@user`, Direct plans of mutual funds have no commission, and fees are lower compared to its Regular plan counterpart. Returns are higher with no extra risk. [Read this for more details](https://indiainvestments.gitbook.io/content/faqs/mfs/direct-vs-regular)                                                                                                       |
| `.bestmf`       | *Which is the best mutual fund?*, *What MF should I invest in?*                                               | Hello `@user`, no one can predict how a mutual fund would perform in the long run. Data also shows consistently chasing best mutual funds result in behaviour gap. Pick one that you can stay with for long term. Learn more [here](https://indiainvestments.gitbook.io/content/faqs/whats-the-best-mutual-fund-i-can-invest-in)                                             |
| `.sipdate`      | *Which day of the month gives best returns for SIP?*                                                          | Unfortunately, there’s no such thing, `@user`. It’s rare for markets to move up / down so much in a single month, that a single SIP installment being on a different date would make a size-able difference in your long term. Read [more here](https://indiainvestments.gitbook.io/content/faqs/which-date-s-is-are-best-for-sip-in-a-month)                                |
| `.dematmf`      | *How good is Coin for MFs?*, *Is there any downside in using Coin?*                                           | `@user`, you should avoid Demat mode of holding when it comes to mutual funds. Learn more [here](https://indiainvestments.gitbook.io/content/faqs/should-i-get-a-demat-account-to-buy-units-in-mutual-funds)                                                                                                                                                                 |
| `.chit`         | *Should I invest in a chit fund?*, *What kind of returns can I expect from a chit?*                           | Hey `@user`, we have some discussions on chit funds [here](https://indiainvestments.gitbook.io/content/faqs/explain-like-i-am-5-eli5-chit-funds.). If you have more queries about chit funds, you can ask in #general-talk after reading this :)                                                                                                                             |
| `.bestelss`     | *Which ELSS fund should I invest in?*                                                                         | Hello `@user`, ELSS investment is already capped at 1.5L per year. And if the investment principal is small, the return difference wouldn’t be large. Just pick one, you’re as likely to be wrong as you could be lucky. Read more [here](https://indiainvestments.gitbook.io/content/faqs/ive-to-invest-in-elss-for-80c-tax-saving.-which-fund-s-should-i-pick)             |
| `.lic`          | *Should I invest in this LIC policy?*                                                                         | `@user`, avoid. LIC and the agent would take most of it. You’d be left with peanuts. It’s one of the most opaque forms of investment, and there’s no guarantee. Govt. backs LIC, not your financial future. Learn more [here](https://indiainvestments.gitbook.io/content/faqs/should-i-invest-in-this-lic-policy)                                                           |
| `.wealthplan`   | *My bank is offering me this lucrative plan, should I invest?*                                                | `@user`, we would suggest you avoid such plans. Insurance companies and bank RMs would make gains, but you could do much better not mixing insurance with investments. Insurance cover is inadequate, returns from ULIPs are lower than bank deposits. Read more [here](https://indiainvestments.gitbook.io/content/faqs/opinions-on-investing-in-smart-wealth-plan-by-bank) |
| `.gold`         | *Good time to buy gold?*                                                                                      | Hey `@user`, if you’re wondering whether it’s time to buy Gold, you might want to [check this out](https://indiainvestments.gitbook.io/content/faqs/is-gold-a-good-investment-now-it-has-gone-up-50-this-year.)                                                                                                                                                              |
| `.smallcase`    | *Is smallcase a good investment?*                                                                             | Hey `@user`, while smallcase has tools which can aid in managing a stock portfolio better than most brokerage options, do your own due diligence before you invest in a smallcase because the CAGR looks great. Read more [here](https://indiainvestments.gitbook.io/content/faqs/is-smallcase-a-good-investment-returns-look-good.)                                         |
| `.itr`          | *I don’t have any tax to pay this year, do I still have to file ITR?*                                         | Hey `@user`, we recommend filing an ITR anyway. Read [more here](https://indiainvestments.gitbook.io/content/faqs/i-dont-have-any-tax-to-pay.-do-i-still-have-to-file-itr)                                                                                                                                                                                                   |
| `.sipvslump`    | *Which one is better - SIP or Lumpsum?*                                                                       | `@user`, if you’re investing for the long term, time in the market beats timing the market. Invest the entire amount all at once, irrespective of market levels. Invest regularly if don’t have lumpsum. Learn more [here](https://indiainvestments.gitbook.io/content/faqs/lumpsum-investment-vs-sip-dca.)                                                                  |
| `.park`         | *Where can I park money for a few days?*                                                                      | Hey `@user`, read about different ways to park money for shorter duration [here](https://indiainvestments.gitbook.io/content/faqs/where-can-i-park-money-for-a-few-days-a-few-months-or-a-few-years)                                                                                                                                                                         |
| `.stock`        | *Why am I not able to send messages to #stock-fundamentals*                                                   | Hey `@user`, if you’re wondering why you’re not able to send messages to #stock-fundamentals channel, please [read this first](https://indiainvestments.gitbook.io/content/faqs/i-cannot-send-messages-to-stocks-fundamentals-channel-on-discord.-why)                                                                                                                       |
| `.maxtermcover` | *Up to what age should I take term cover?*                                                                    | `@user`, short answer is - till the age someone is financially dependent on your income. Ideally, it should be 60-65. Read more [here](https://indiainvestments.gitbook.io/content/faqs/up-to-what-age-should-i-take-term-cover)                                                                                                                                             |
| `.grouppolicy`  | *Should I have my own health insurance, even if employer provides one?*                                       | `@user` - yes, you should have your own. Employer-provided group policy might have lower cover, or co-pay, or a cap on room-rent. You should get one on your own, to decouple your insurance from your employer. Learn more [here](https://indiainvestments.gitbook.io/content/faqs/do-i-need-my-own-health-insurance-employer-already-has-group-policy)                     |
| `.mfapp`        | *Should I use app X or Y for MF investing? Is this hot app Z good?*                                           | Hey `@user`, as long as the platform allows buying direct plan in growth schemes (for free of cost), pick one you’re comfortable with. Your specific choice of app won’t affect your returns. We have covered pros & cons of popular apps [here](https://indiainvestments.gitbook.io/content/faqs/best-mutual-fund-app-for-investmentsy)                                     |
| `.stockapp`     | *Should I use Zerodha or Upstox?*                                                                             | Hey `@user`, use a discount broker like Zerodha. If you need more detailed comparison on popular discount brokers, especially how they stack up against each other on fees and transfer charges, [check this out](https://indiainvestments.gitbook.io/content/faqs/what-is-the-best-app-for-buying-or-trading-stocks)                                                        |
| `.uswhy`        | *Should I invest in US markets? I'm already investing in mutual funds in India*                               | Hey `@user`, US equities give diversification and exposure to global growth in the most stable currency. You should invest in US equities, if you can find a cost-effective way to do it. [Read more here](https://indiainvestments.gitbook.io/content/faqs/why-should-i-invest-in-the-us-markets)                                                                           |
| `.ushow`        | *How should I invest in the US markets? Should I open a Vested account? Or just invest in Motilal N100 fund?* | Hey `@user`, invest in a cost-effective manner. For smaller corpus, it makes sense to invest via India-domiciled mutual funds that invest overseas, while when you've a larger amount to invest, it could be cheaper to invest directly via US-based brokers. [Details here](https://indiainvestments.gitbook.io/content/faqs/how-should-i-invest-in-us-equity).             |

For example, if someone asks (let's say, user name is `@beginnerinvestor`) *hey guys, should I buy this LIC policy?*, you can respond with `.lic @beginnerinvestor`.

Bot would delete your message, and add its own message, tagging `@beginnerinvestor`

{% embed url="https://youtu.be/QJxJVEU6D48" caption="Invoking the bot for FAQ in Discord - Dark Mode" %}

{% embed url="https://youtu.be/Jh9WnK6FPL4" caption="Invoking the bot for FAQ in Discord - Light Mode" %}

## Pre-requisites ✋

We expect you to familiarize yourself with all the FAQs, before starting with this.

You can go through our FAQs using below link

If you're using the bot to invoke the FAQ, it's expected that you've yourself at the very least gone through that FAQ first.
