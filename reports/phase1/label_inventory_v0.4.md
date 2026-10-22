# Label inventory v0.4

Examples are verbatim excerpts of real corpus records. Each Arabic example is followed by our English translation; inshallah is left untranslated because its function is what the label records. The source reference of each example is listed in label_examples.csv, and the extraction notebook pulls each example from its source record. These are illustrative judgments, not gold Phase 3 annotations.

## COMMIT

An explicit undertaking or intention concerning the speaker’s own future action.

- ورايح ان شاء الله أجيب الدواء (sada, train.csv:184833)  
  “And I’m going, inshallah, to get the medicine.” — Own stated future action to obtain medicine.
- أنا أبلغه ان شاء الله (sada, train.csv:197199)  
  “I’ll tell him, inshallah.” — Speaker undertakes notifying Ibrahim.
- راح ارتبط فيه ان شاء الله (sfc, 24.txt:115470)  
  “I will stick with it, inshallah.” — Explicit intention to stay within the speaker’s specialization.
## WISH

A hope or blessing about an outcome the speaker does not control, favourable or unfavourable, including a blessing at the end of a turn or post.

- يا رب إن شاء الله يوفقك يا وليدي ويسعدك (sada, train.csv:227867)  
  “O Lord, inshallah He grants you success, my son, and makes you happy.” — Concrete blessing for success and happiness.
- ربي يوفقك ويسهل لك دربك وامرك ان شاء الله (sfc, 24.txt:94381)  
  “May my Lord grant you success and ease your path and your affairs, inshallah.” — Concrete blessing; final sentence position does not make it CLOSE.
- وان شاء الله تتيسر اموركـ (sfc, 52.txt:111424)  
  “And inshallah your affairs will go smoothly.” — Hoped-for favourable outcome beyond direct speaker control.
## DEFER

A noncommittal postponement or evasive answer about a requested action or response.

- أنا دارسها ومرتب لها إن شاء الله إن شاء الله محلولة (sada, train.csv:191417)  
  “I’ve studied it and arranged for it, inshallah; inshallah it’s settled.” — Asked when a debt will be repaid; gives reassurance without a date.
- أنا إن شاء الله بعدين افهمك (sada, train.csv:215316)  
  “Inshallah I’ll explain it to you later.” — Asked what is happening; explicitly postpones the explanation.
- ايه ان شاء الله ان شاء الله (sada, train.csv:131578)  
  “Yes, inshallah, inshallah.” — Pressed for exact investigation details, shifts to praising the project; speaker turns remain noisy.

COMMIT versus DEFER: if the reply names the act or confirms that it will be done, the label is COMMIT, even when the speaker is reluctant or adds a condition; if the reply to a request or question leaves the act, its time or the speaker’s intention open, the label is DEFER. DEFER versus SKEPTIC: if inshallah answers a request for the speaker’s own action and leaves it unsettled without irony, the label is DEFER; if it doubts or mocks a claim, plan or expectation, whether someone else’s or the speaker’s own when explicitly undercut (e.g., تحلم), the label is SKEPTIC.

## HEDGE

Epistemic qualification of a present or past assessment.

- ان شاء الله يكون وضحت لك (sfc, 26.txt:10442)  
  “Inshallah I have made it clear to you.” — Tentative assessment of explanation already given.
- إن شاء الله الحسابات طلعت مظبوطة يا عمي (sada, test.csv:6162)  
  “Inshallah the calculations came out right, uncle.” — Tentative assessment of completed calculations.
- بس إن شاء الله ما يكون فات ألأاون (sada, train.csv:188757)  
  “But inshallah it is not already too late.” — Tentative assessment that it is not already too late.
## SKEPTIC

An ironic or doubting use that undercuts an apparent claim, promise or expectation, including an explicitly self-mocked intention.

- ان شالله لما يسمحوا لنا أوريكم الفلة على أصولها <<<< تحلم ههههه (sfc, 14.txt:54146)  
  “Inshallah, when they let us, I’ll show you the villa properly <<<< dream on hahaha” — Historical Saudi forum context; apparent intention explicitly undercut as a fantasy.
- متى كنت ناوي تبيع ان شاء الله (sfc, 51.txt:121424)  
  “When, inshallah, were you planning to sell?” — Rhetorical reproach after شريت بالقيمه هذي ومابعت; ironic questioning rather than a literal future request.
- وتبغينا نهرب و فين نروح إن شاء الله (sada, train.csv:227627)  
  “And you want us to run away? And where would we go, inshallah?” — Incredulous response to escape suggestion, followed by في أي عصر; noisy dialogue needs confirmation during Phase 3.
## CLOSE

A conventional acknowledgement or topic ending without a new action or hoped-for outcome.

- طيب ان شاء الله. (sada, train.csv:203201)  
  “OK, inshallah.” — Acknowledges the previous exchange without a new action or positive outcome.
- ان شاء الله شكرا للمرور (sfc, 54.txt:61390)  
  “Inshallah. Thanks for stopping by.” — Formula followed solely by thanking the visitor.
- فإلى الغد ان شاء الله (sfc, 49.txt:17367)  
  “Until tomorrow, inshallah.” — Ends the writer’s current session without specifying a new task.

WISH versus CLOSE: if inshallah attaches to a specific outcome outside the speaker’s control, the label is WISH, even at the end of a turn; if it adds no new outcome and only acknowledges or closes the exchange, for example before thanks, leave-taking or a topic shift, the label is CLOSE. HEDGE versus WISH: if the proposition concerns an existing state, the label is HEDGE; if it concerns a hoped-for future result, the label is WISH. Laughter alone never proves SKEPTIC.


## OTHER, UNCLEAR and QUOTE

OTHER records recognizable functions outside the six labels, such as threats, curses or warnings. UNCLEAR is used only when the context is not enough to decide, not for a known function. QUOTE marks Quranic quotations, which are excluded from annotation. Source membership alone does not establish individual dialect or nationality.
