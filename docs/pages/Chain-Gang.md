---
title: Chain Gang
layout: default
navigation_weight: 9
---
# Chain Gang

**Ivy** is a programming language designed to code and convert block chain technology into the lower level byte language of the **Chain Virtual Machine**, or **CVM**.

{% include md-toc-flammarion.htm %}

## CVM

The **Chain Virtual Machine** aka the **CVM** drives the Turing complete **Chain**  platform developed by the **Chain Gang** at [Chain dot com](2).

The same restriction applies to runaway contracts when using the **CVM** as when using the **Ethereum Virtual Machine**, or **EVM**.

However, unlike the **Ethereum** platform, the *gas* is free when using the **Chain dot com** platform.

This is a test sentence for the internal page anchor #1 in red => MMINAIL [[1](#MMINAIL){:.red}].

The reference points to the first internal citation [[MMINAIL](#MMINAIL){:.red}] below.

By clicking on either the red [1] above, or the red [MMINAIL] ...
{:.red}

The reader will be hyperlinked to the bottom of the page directly to the referenced citation.

## Receiver Objects

A **Receiver Object** is a node that issues a digital form of invoice to an *incoming party*.

The *incoming party* resides externally to the **Receiver Object** on the network and is sending a message to the **Receiver Object** to please accept coin.

The message being read by the *receiving party* is an attempt to engage one or more methods that are located on the **Receiver Object**.

The overture to accept coin from the *incoming party* needs to be acknowledged by the *receiving party* before a transaction can take place.

In other words, an external party to a contract cannot simply toss a coin at another node on the network without an acknowledgment from the *receiving party*.

A protocol must be established to either accept the incoming asset if desirable, or to reject the incoming asset if by some other method the sender is deemed not worthy.

## Serialize and Send

First, we have to create a **Receiver Object** with the keyword "Receiver", as follows:

```liquid
{% raw %}
Receiver robin = new Account.ReceiverBuilder()
{% endraw %}
```

Here, we have initialized our **Receiver Object** with the name `robin`and we have assigned the value of the return from the new Account ReceiverBuilder method to our new `robin` **Receiver Object**.

### Fleshing It Out

The authors at the **Chain Gang** have let the end-user sink or swim with the balance of the code, at this juncture.

```liquid
{% raw %}
Receiver robin = new Account.ReceiverBuilder()
  .setAccountAlias("castle")
{% endraw %}
```

And, further ...

```liquid
{% raw %}
Receiver robin = new Account.ReceiverBuilder()
  .setAccountAlias("castle")
  .create(client);
{% endraw %}
```

And, more ...

```liquid
{% raw %}
Receiver robin = new Account.ReceiverBuilder()
  .setAccountAlias("castle")
  .create(client);

String castleReceiverSerialized = castleReceiver.to_Json();
{% endraw %}
```

More code ...

```liquid
{% raw %}
Receiver robin = new Account.ReceiverBuilder()
  .setAccountAlias("castle")
  .create(client);

String castleReceiverSerialized = castleReceiver.to_Json();
  castle_receiver = chain.accounts.create_receiver
    account_alias: 'castle'
  )
{% endraw %}
```

Still more ...

```liquid
{% raw %}
Receiver robin = new Account.ReceiverBuilder()
  .setAccountAlias("castle")
  .create(client);

String castleReceiverSerialized = castleReceiver.to_Json();
  castle_receiver = chain.accounts.create_receiver
    account_alias: 'castle'
  )

 castle_receiver_serialized = bob_receiver.to_json
{% endraw %}
```

Keep it coming, line by line, method by method ...

```liquid
{% raw %}
Receiver robin = new Account.ReceiverBuilder()
  .setAccountAlias("castle")
  .create(client);

String castleReceiverSerialized = castleReceiver.to_Json();

  castle_receiver = chain.accounts.create_receiver(
    account_alias: 'castle'
  )

  castle_receiver_serialized = bob_receiver.to_json

  const castleReceiverSerializedPromise = client.accounts.createReceiver(
    {
      accountAlias: 'castle',
    }
  ).then(castleReceiver => {
      return JSON.stringify(castleReceiver)
    }
  )
{% endraw %}
```

### Receiver Request: Creation

A **Receiver Request** is the message to the **Receiver Object** to please accept coin.

```liquid
{% raw %}
Transaction.Template spendingTransaction2 = new Transaction.Builder()
//
  .addAction(new Transaction.Action.SpendFromAccount()
    .setAccountAlias("mminail")
    .setAssetAlias("medcoin")
    .setAmount(1)
  ).addAction(new Transaction.Action.ControlWithReceiver()
    .setReceiver(Receiver.fromJson(castleReceiverSerialized))
    .setAssetAlias("medcoin")
    .setAmount(1)
  ).build(client);
//
{% endraw %}
```

### Receiver Request: Submission

Notice how the **Receiver Request** above includes a call to the pre-made 'castleReceiverSerialized' method.

```liquid
{% raw %}
`...`
{% endraw %}
```

## Raw Code

Place the introducing line of text ie.) the 'tagline' here ...

```liquid
{% raw %}
`...`
{% endraw %}
```

## Sources and Uses

The source and use of 3rd party materials in the creation of this **Markdown** page is greatly appreciated.

Most authors and publishers will allow for the abbreviated reproduction of their works in part when the case of brief quotations or ideas embodied in critical articles or reviews becomes necessary to further the understanding of the end-user's learning process.

Indeed, ping-backs to the original sources are welcome by the readers, the authors, and the publishers of instructional hard copies.

Therefore, it is the policy of the MMINAIL [[1](#MMINAIL){:.red}] to always provide a **Ping Back** to the original author, or to the publisher of the original publication when citing 3rd party work.

### Inline References

1. {:#MMINAIL}The [MMINAIL](https://mminail.github.io/){:title="Click to Visit the Concept Library of the Medical Marijuana Initiative of North America - International Limited, an Arizona Benefit Corporation"}{:target="_blank"} is an acronym for the Medical Marijuana Initiative of North America - International Limited, an Arizona Benefit Corporation. Published by © 2017 [Mminail.github.io](https://mminail.github.io/){:title="Click to Visit the Concept Library of the Medical Marijuana Initiative of North America - International Limited, an Arizona Benefit Corporation"}{:target="_blank"}.

1. The [CHAIN](https://www.chain.com/){:title="Click to Visit Chain dot com"}{:target="_blank"} is an acronym for the Chain Virtual Machine and its accompanying Ivy programming language. Published by © 2017 [Chain.com](https://www.chain.com/){:title="Click to Visit Chain dot com"}{:target="_blank"}.

### External Sources

- The [Project Source Links](https://mminail.github.io/Ivy/Source-Ivy-Links.htm){:title="Click to Visit the Ivy Lessons Project Source Links page"}{:target="_blank"} for the Ivy Lessons Project. Published by © 2017 [Mminail.github.io](https://mminail.github.io/){:title="Click to Visit the Concept Library of the Medical Marijuana Initiative of North America - International Limited, an Arizona Benefit Corporation"}{:target="_blank"}.

**Note**. Please support the authors and publishers who aggregate the **Source Links** for our projects.
