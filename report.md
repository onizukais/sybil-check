

Independent Clusters


It is important to understand that each cluster in this report is independent, with its own description and argumentation. While creating a separate issue for each cluster would be ideal, it is not feasible as it would result in my account being flagged for spam on GitHub. Therefore, please evaluate each cluster independently and pardon any changes necessitated by the report's size.

Detailed Methodology and Walkthrough


Data Collection

To gather data, I utilized explorers to compile as many CEX (Centralized Exchange) hot wallets (from Binance, Coinbase, Kucoin, Bybit, OKX) and gas suppliers as possible. A simple SQL query on Dune was then used to collect approximately 2.5 million CEX deposit addresses (addresses where users send assets to deposit into a CEX).

Initial Filtering

Using the Dune Dashboard, I filtered these CEX deposit addresses to identify those that had received funds from at least seven addresses interacting regularly with Layer Zero. Clusters of active L0 addresses, ranging from 7 to 300, sharing the same CEX deposit address, were identified and used to form larger clusters. This was done by incorporating addresses that interacted with cluster addresses but not directly with the CEX deposit address. To minimize false positives, an address had to be directly linked to at least four other cluster addresses to be included. Clusters with fewer than 20 addresses (including the CEX deposit address) were discarded.

Detection and Proof - Layer One

The first detection layer involves automated scripts that group addresses sharing the same CEX deposit address and being linked to at least four other addresses within the cluster. Despite its automation, this layer still has a percentage of false positives due to multiple interactions and the common CEX deposit address.

Detection and Proof - Layer Two

The second detection layer involves manual verification. Each address within a cluster was manually scanned to remove false positives and add on-chain arguments to the cluster description. These arguments varied, including the execution of the same transactions at the same time with the same amounts and similar transaction patterns for L0 activities. Multiple resources, such as LayerZero Scan, Dune, Debank, Arkham, and Etherscan, were utilized for this purpose.

Although this manual process is time-consuming, it ensures the sybil nature of the clusters and minimizes false positives. It also demonstrates that substantial work has been done, rather than merely providing a large list of addresses.

Combining Layers for Accurate Detection

By combining both detection layers, we achieve reliable detection with minimal false positives. The clusters' use of the same CEX deposit address and manually reported on-chain activities significantly enhance the accuracy of the results.

Blockchain Activity Screening

The activity predating the snapshot was screened across 14 blockchains, including:

Ethereum: end block 19757726

Optimism: end block 119326917

BSC: end block 38236464

Polygon: end block 56379454

Arbitrum: end block 205653169

Gnosis: end block 33677943

Linea: end block 4059728

Scroll: end block 5184468

Zksync: end block 32656745

Moonbeam: end block 6045324

Moonriver: end block 6637617

Fantom: end block 80127182

Base: end block 13709885

Celo: end block 25273962

Notes on Arkham Diagrams

Please be aware that links in Arkham diagrams within this report may often be missing, as Arkham only supports 7 out of these 14 blockchains.


Reward Address (If Eligible)

0x5B823c2e656A3deFB87847036faEa6Dc20899966

This is a fresh address.



CLUSTER 26

The first 8 addresses of the cluster share the same Binance deposit address: 0x96c167D92bE4068940e8036f8CeAf91d0b6AAEF8. The remaining addresses are linked to numerous other addresses within the cluster multiple times.


```
0xf086748cfcdccd1efa72f8b12e50547cfe174913
0xd4648afa05071c7e2c3e74e64b017bf0291be3a6
0x6bb9e127e0a68f1644a873208097258157bae49d
0x8f9fe2408a3715bcb8f59fe0c4fcac186399f7bd
0xb54defad873c1df316fd61d0ed85974585c11795
0xc0aac4ec8335d78dd049ec5d99178106d7d654fc
0x646e3bd22b9d2c40de855dc467af1528307ae4d5
0x6b47a326f049f0c7c7666f05631106daf967d64f
0xbf022b19a5d389b0129bc6d0856051ad4838f986
0x0229a3d4fab214ac8ae4fe6a5bb1b7279592ac9d
0xd0be5393d1a423e2761225cabb62a6fa81d5fdc0
0xd95417aa3023043931328d5a3baa6afd80379510
0x4060c69936e04075dc6170c4d5b1fe3e35a4baab
0xa343330f1e2848f02d09ad0f197be4f75ecdfb3c
0xc3f7debf793001d97badbd056e038fc5d9424689
0x052321f8fd145e193243e18986abfbc411c0d0d5
0xce50bb4b0364804bf06e98b4ba41553f50df0d72
0xdefd213b17192e57eeb77da9ae1c22a2fbd96bee
0x7bfbcb4e840ac0ff776b2076b1059bd97e991259
0x601ae641d4db4dc5f13dc06f5cab0b767071ba33
0x646e3bd22b9d2c40de855dc467af1528307ae4d5
0xfe0d44e5cb1d0ac5e75657f57da993edd67ee618
0x6ae4c746a66f8d41564ecc34159e83c2ca5ea0d2
0x2492faede662f1a23bba2a3e271d4b4a52e39a85
0x8b39225eab9c463e0b00c61acf1d489def2ccca7
```

 ![cluster1](https://github.com/onizukais/sybil-check/assets/170208261/650a0dc3-e6a5-4ad0-98a2-1d769bd0427f)



 All these addresses exhibit the same on-chain activity. They execute the same transaction while using the same bridge (Arbitrum Nova Bridge) on the same time period. This suggests a large-scale sybil operation, likely automated by scripts.


<img width="979" alt="Capture d’écran 2024-05-19 à 21 41 19" src="https://github.com/onizukais/sybil-check/assets/170208261/5b2679f8-4ab0-47e6-8934-a8baaf8b503b">
<img width="967" alt="Capture d’écran 2024-05-19 à 21 42 06" src="https://github.com/onizukais/sybil-check/assets/170208261/801efa8e-0932-45e2-951f-a7dbee9264f8">
<img width="969" alt="Capture d’écran 2024-05-19 à 21 42 56" src="https://github.com/onizukais/sybil-check/assets/170208261/775bed38-60ea-4339-ab3a-d6a469ddb0e8">
<img width="982" alt="Capture d’écran 2024-05-19 à 21 43 19" src="https://github.com/onizukais/sybil-check/assets/170208261/a8bd2aca-a66c-43c4-ad44-6276b2e0dae1">
<img width="982" alt="Capture d’écran 2024-05-19 à 21 47 07" src="https://github.com/onizukais/sybil-check/assets/170208261/ad42aeae-49f4-458c-a8f4-74428113006a">
<img width="953" alt="Capture d’écran 2024-05-19 à 21 47 31" src="https://github.com/onizukais/sybil-check/assets/170208261/f24e26b6-3ac1-4d02-80cd-54352a62f825">
<img width="965" alt="Capture d’écran 2024-05-19 à 21 47 59" src="https://github.com/onizukais/sybil-check/assets/170208261/4416cfe3-aa4e-497a-916b-b918fdb2d38b">
<img width="1002" alt="Capture d’écran 2024-05-19 à 21 48 20" src="https://github.com/onizukais/sybil-check/assets/170208261/478a42b8-2d1b-4409-8aa8-59a9fe125e9b">
<img width="980" alt="Capture d’écran 2024-05-19 à 21 48 38" src="https://github.com/onizukais/sybil-check/assets/170208261/9fec72d4-7bec-40c4-936a-e3a04ed1f7bd">
<img width="961" alt="Capture d’écran 2024-05-19 à 21 50 08" src="https://github.com/onizukais/sybil-check/assets/170208261/d5586b07-791c-4e09-9dd4-2ec604f80561">
<img width="1015" alt="Capture d’écran 2024-05-19 à 21 40 49" src="https://github.com/onizukais/sybil-check/assets/170208261/8727e545-89f3-49b1-802a-7053dbccc3b4">
<img width="945" alt="Capture d’écran 2024-05-19 à 21 41 41" src="https://github.com/onizukais/sybil-check/assets/170208261/0bfac484-0d0b-4bd0-9ba7-cf8a1a40875d">

Then, we can notice another transaction pattern which appear on the cluster's wallet, again, the transactions are made on the same chain, on the same period and the same address appears on it ( 0xddd41bcd80feb8b02e46bada482eb6afd433aff7 )

<img width="988" alt="Capture d’écran 2024-05-19 à 22 03 28" src="https://github.com/onizukais/sybil-check/assets/170208261/73c58759-5560-4b55-b377-9121fff5927a">
<img width="968" alt="Capture d’écran 2024-05-19 à 22 04 13" src="https://github.com/onizukais/sybil-check/assets/170208261/7b63d7ca-633d-4dd7-ba7a-159827de7232">
<img width="979" alt="Capture d’écran 2024-05-19 à 22 04 50" src="https://github.com/onizukais/sybil-check/assets/170208261/834853fe-fc1d-47b1-b78d-79655cd2c820">
<img width="979" alt="Capture d’écran 2024-05-19 à 22 05 16" src="https://github.com/onizukais/sybil-check/assets/170208261/2305f19d-3de2-470e-9f56-4c9b1b0b17a5">
<img width="958" alt="Capture d’écran 2024-05-19 à 22 05 47" src="https://github.com/onizukais/sybil-check/assets/170208261/1aa97074-3849-4fa8-82ff-97e3c4a70846">
<img width="980" alt="Capture d’écran 2024-05-19 à 22 06 10" src="https://github.com/onizukais/sybil-check/assets/170208261/5479687c-f188-4fed-82bd-51329d99fc4a">
<img width="947" alt="Capture d’écran 2024-05-19 à 22 08 36" src="https://github.com/onizukais/sybil-check/assets/170208261/c7ea84a9-25db-4348-9aa4-3ff089dfc1f5">
<img width="963" alt="Capture d’écran 2024-05-19 à 22 09 00" src="https://github.com/onizukais/sybil-check/assets/170208261/9de28f91-bb18-4076-b561-96b774aa017e">

Cluster + same CEX deposit address + same on-chain activity at the same time, this is without a doubt a sybil operation.




CLUSTER 50


The first 5 addresses of the cluster share the same OKX deposit address: 0xD82b6ec56B76D5cA43D7826dce4e3d2Ff9C173DE. The remaining addresses are linked to numerous other addresses within the cluster multiple times.

```
0xb087e0033db8c075d9267e543c9e3b9f19bcc7f9
0x2caaa9c911de5990b474eb5c7679b8662d931eb2
0xe21b36ebede73eb8acc7e15e13407d629240cfbf
0xbb3a0ceeea78fc630ea6ac4c97eecd106aefa16e
0x0b61e8ce1efc73078db28b8dc9ae6e635efe67dd
0x227fbcb2931d501a31f29b1a356e12f71c6deb8d
0x68db90264b5f95032110965e2b4ca7353d67f9f5
0x8cb50b46e0708dc0b2b34e6077b876eb95a057af
0xe2709b901d6ea39ffca044679b4e268f65c68661
0xf59a93cf770eb6e2b4344387ce835c58ff8b363d
0x2d232c211c80c8ce716b884b8fcd784bb55e6053
0x4f2dc64360ebbe78c968338ed4baae1d14144340
0xa69bde39bafa75534befd12a5f36ec8f95248009
0xad8a954fab2e71f3865a8272c4042e10d83e3d5f
0x0941f8f756e890b2d81f7f16970a872ce0ae4001
0x9aa1575e60d33cd8e750f3193bdfa7d5540fe136
0x3485f5b66360022b56382cb7f37424f5f8f76ee7
0x45b0c219918c42f0ca946bdb91b517275a8c9cca
0xe0735dc521947f398d26184df05ca3803474eefd
0xb339297171670de477002e1e3bd429b87d2da263
0x8d8979ba8c18e0591f08cdefa54980a13b71df1b
0xdb520b6769df9df5911e5969d570ea12850dac69
0x48996d180fda73c5d44ac0b92cae7022b84a9acb
0xfc03f894465e2b43be15a56918c4e298e2ee4be5
0x50270d3eea45820a33e7b57072e49c37f0fbf40e
0xfd0041184f9387a822216be34da1f4893ea7b426
0xf3b5f18add21b6578e679d0de8ac7597d0095b73
0x6a643bcc171e12448aa4202db2bfd4b008108a5a
0xd12c62dea4f5c705b38f4b034c3561ca65be71d5
0x897aaceb5620805a04b561c076ca49667d663238
0x1d639c172c474d56ef85dae0431295466734c197
0xc6cbb0774096f5309dcea918b30b32e194cbebc1
0xa050e41f634170149c3b151729260df037a0f946
0x76fc58dd26ed16baf40a893faef7920afd679036
0x6fbca37a3d4933f1ec9419a4c3da5d5329cddfc2
0x2a89216e0135be6cae98fb207cb024b96de980c3
```

![n](https://github.com/onizukais/sybil-check/assets/170208261/295e3410-de54-49e9-b1d3-2e8e4fc53b95)


 


These addresses exhibit the same on-chain activity. 

<img width="1497" alt="Capture d’écran 2024-05-19 à 22 22 13" src="https://github.com/onizukais/sybil-check/assets/170208261/b521be21-fbda-454a-82db-1ffe02be74f1">
<img width="1479" alt="Capture d’écran 2024-05-19 à 22 22 29" src="https://github.com/onizukais/sybil-check/assets/170208261/ebbb999b-5d66-4e84-aac4-49794539a8ad">
<img width="1509" alt="Capture d’écran 2024-05-19 à 22 22 41" src="https://github.com/onizukais/sybil-check/assets/170208261/14675c05-7de8-4f2e-bc9d-0a67cb4b9816">
<img width="1497" alt="Capture d’écran 2024-05-19 à 22 22 59" src="https://github.com/onizukais/sybil-check/assets/170208261/1b535371-df82-4be1-9ca6-419b2ed07e39">
<img width="1507" alt="Capture d’écran 2024-05-19 à 22 23 11" src="https://github.com/onizukais/sybil-check/assets/170208261/53dfaee3-8a0c-420b-b338-69d2db7eb700">
<img width="1512" alt="Capture d’écran 2024-05-19 à 22 23 25" src="https://github.com/onizukais/sybil-check/assets/170208261/6571692d-2d0d-4caf-9503-a3762381aa3f">
<img width="1496" alt="Capture d’écran 2024-05-19 à 22 24 41" src="https://github.com/onizukais/sybil-check/assets/170208261/58fd3334-740d-464e-af1f-26979e9a08fa">
<img width="1501" alt="Capture d’écran 2024-05-19 à 22 24 54" src="https://github.com/onizukais/sybil-check/assets/170208261/7d9f3170-3a93-485e-b962-02ec124d550c">

<img width="1508" alt="Capture d’écran 2024-05-19 à 22 25 04" src="https://github.com/onizukais/sybil-check/assets/170208261/5f156c8d-eaf7-432d-ba99-efb5a549ee3a">

   
For example, their most recent Layer Zero interactions are the same, with the same dapps used at the same time in the same order: Merkly 18 days ago, Stargate 4 months ago, Merkly 6 months ago. 

We can also notice that the cluster's wallet used Stargate Arbitrum on the same date period 

<img width="968" alt="Capture d’écran 2024-05-19 à 22 37 19" src="https://github.com/onizukais/sybil-check/assets/170208261/b0dab81d-5f76-4ba8-bebb-0f750b40757a">
<img width="975" alt="Capture d’écran 2024-05-19 à 22 37 39" src="https://github.com/onizukais/sybil-check/assets/170208261/bb321113-3803-42e0-8753-d1a8ff8b5395">
<img width="1001" alt="Capture d’écran 2024-05-19 à 22 37 56" src="https://github.com/onizukais/sybil-check/assets/170208261/397c2dc1-8314-4558-a08e-3b7967fc860d">
<img width="973" alt="Capture d’écran 2024-05-19 à 22 38 15" src="https://github.com/onizukais/sybil-check/assets/170208261/4ed8c9a0-b46e-49ef-861b-9444acc9f09d">
<img width="974" alt="Capture d’écran 2024-05-19 à 22 38 55" src="https://github.com/onizukais/sybil-check/assets/170208261/5193637b-ce4b-4a7a-b1ef-68343ea07c55">
<img width="950" alt="Capture d’écran 2024-05-19 à 22 39 18" src="https://github.com/onizukais/sybil-check/assets/170208261/7ed19406-edff-4e27-9458-2ed05c5bff1c">
<img width="963" alt="Capture d’écran 2024-05-19 à 22 42 30" src="https://github.com/onizukais/sybil-check/assets/170208261/b2eba45a-805e-4fd0-8828-0ff17db8caf3">
<img width="943" alt="Capture d’écran 2024-05-19 à 22 42 46" src="https://github.com/onizukais/sybil-check/assets/170208261/95e3d177-d4f2-48aa-bde7-3e9803644f50">
<img width="1002" alt="Capture d’écran 2024-05-19 à 22 43 02" src="https://github.com/onizukais/sybil-check/assets/170208261/d5ee02b7-cfce-4077-8092-6c56e1163818">
<img width="986" alt="Capture d’écran 2024-05-19 à 22 43 19" src="https://github.com/onizukais/sybil-check/assets/170208261/f120598d-78ab-42de-9211-5b3f15749134">


These addresses share the same CEX deposit address, are part of a cluster with multiple internal links, and exhibit the same on-chain behavior. This suggests a large-scale sybil operation, likely automated by scripts.

 

 
 


 

CLUSTER 51

The first 7 addresses of the cluster share the same Binance deposit address: 0xDEa00B50ef00397c585a4A571585A3cecdCC8f5f. The remaining addresses are linked to numerous other addresses within the cluster multiple times.

```
0x80e82eabe9661b8486c87fed697c2151fdfe2bb1
0xfcffc4bae29e75f108e2496afdfa8ac150a6985a
0xebdd26127ae02a4e01ce45ef7df2fb4cb2749de6
0xf3ff1be41319aa44a759fc59d7be1be3c8b34bd5
0xcae03f27fbefef8d209b4424fae8aa9012079170
0x8d8c74bef923b63c393ae4b7bbf249442ce0fd59
0x20a9e5517c5c9a464da5a0750d2b5d381f373ebc
0x68ee33a5491259acb20a280f74b6858315f8bae1
0xb519d7664d1b862bb8f118d138bd43123c7b4b07
0x034fed0e84e250cccf5dc21a14511b212a54bddb
0x8e2da4a20777a22b2c6c4f159ea265a4b15fefdd
0x387f49fdae110c14c3503e4cc2e72d9ab8f4dab9
0x6891e9536f1fb44a7f6bcfa4d910b95147d137e0
0x0c0ce68d7bd507f5ffe4fbff00b5476d2477ff11
0x62b285bf4e04077da564cd4ba999a605668c6c8e
0x2be4644510db08a8c885e36e524dfa3b2d363d3c
0x2e645e4ee4609dc5e2e3c090cf61bf40e910139c
0x2761d36894600153c5e5e780a059eecbdda66679
0x09bc739bfa9f0a101f5f92a0f16ffc729b97211a
0x7966f650354e716c165381f2cad5d63cef665d31
0xb939db6e80aab2ef86299fc8a20a1c93d03fb0dd
0x7df50c90e392e05736db7f047b50d2f422a062f7
0x750f0efc0a9cce35ba61f23a7dcb678a1b1442b3
0xab81bde2361c9a2564603da7d0315c967aff7ee1
0xae65e17160178833be9c263599486e430dbed510
0xe464168a2318f326d396c67c2549bf54c2749566
0x23db79360ede7fa797d44bfc860f78114a9a67cc
0xed0abfa70b9b9b0d148422584aab8bb48590eeea
0xae20a0eb750bc707ec56e0a48537548a544014c1
0xa7c9e4463043f73af8819dc224104216c4969790
0x592a77f3b94244addfe497ca96769f93e07433df
0xf00e95842c62c938e7f4f0f21e7ce253c7011b97
0xd445b5e58dad7a05c57fda2e3a994a4e7556837b
0xca3d40c72fa7a54a400ddc081ab4440eedd69795
```

 ![ff](https://github.com/onizukais/sybil-check/assets/170208261/f7f4b318-e93f-4756-b48b-abb1f326e617)




These addresses exhibit the same on-chain activity. 

<img width="1512" alt="Capture d’écran 2024-05-19 à 23 22 02" src="https://github.com/onizukais/sybil-check/assets/170208261/3f923b2b-dd8a-4012-b810-cbb938c1fd2a">
<img width="1512" alt="Capture d’écran 2024-05-19 à 23 22 16" src="https://github.com/onizukais/sybil-check/assets/170208261/94fedbb9-1ae4-431b-b51e-1da5b71d0704">
<img width="1512" alt="Capture d’écran 2024-05-19 à 23 22 27" src="https://github.com/onizukais/sybil-check/assets/170208261/c01f0615-b86e-4af3-a90e-a751a9c804c9">
<img width="1512" alt="Capture d’écran 2024-05-19 à 23 22 43" src="https://github.com/onizukais/sybil-check/assets/170208261/7352d07f-b59d-41cf-9785-4ed4157435b1">
<img width="1512" alt="Capture d’écran 2024-05-19 à 23 22 56" src="https://github.com/onizukais/sybil-check/assets/170208261/e7bffb52-db08-4e28-9077-b23360ce2c67">
<img width="1503" alt="Capture d’écran 2024-05-19 à 23 23 08" src="https://github.com/onizukais/sybil-check/assets/170208261/a9be797b-c540-4a1d-a163-a222991e56df">
<img width="1512" alt="Capture d’écran 2024-05-19 à 23 23 21" src="https://github.com/onizukais/sybil-check/assets/170208261/ad203c4e-535d-46e0-b7e5-05de3b444791">
<img width="1511" alt="Capture d’écran 2024-05-19 à 23 23 32" src="https://github.com/onizukais/sybil-check/assets/170208261/55844a62-e6d0-47ab-b1fd-cf8b5155d370">
<img width="1512" alt="Capture d’écran 2024-05-19 à 23 23 44" src="https://github.com/onizukais/sybil-check/assets/170208261/d7e4ae53-6d79-4ef6-80a6-93ffa0627bf0">
<img width="1506" alt="Capture d’écran 2024-05-19 à 23 24 03" src="https://github.com/onizukais/sybil-check/assets/170208261/fb5f4364-c325-42cb-986c-02de956823c0">

Their LayerZero activity is the same. For exemple, most addresses used the same. For exemple, their lastest L0 usage is the same: they used Angle during the same time period.

They also used to provide to stake to the same L0 products in an effort to farm the airdrop. STG & USDC staking on Stargate OP, and USDC on Stargate Avalanche

<img width="986" alt="Capture d’écran 2024-05-19 à 23 39 14" src="https://github.com/onizukais/sybil-check/assets/170208261/56a6e48d-5894-4ce3-b539-97e71e222813">
<img width="1010" alt="Capture d’écran 2024-05-19 à 23 40 21" src="https://github.com/onizukais/sybil-check/assets/170208261/f3d0c402-46e8-4383-bc26-b3b7d9555c98">
<img width="972" alt="Capture d’écran 2024-05-19 à 23 40 34" src="https://github.com/onizukais/sybil-check/assets/170208261/b42325af-5b0d-4295-9eea-712566bcaabd">
<img width="996" alt="Capture d’écran 2024-05-19 à 23 40 48" src="https://github.com/onizukais/sybil-check/assets/170208261/c5a6e7c9-bc4a-47b7-84cb-624041ae25d1">
<img width="1000" alt="Capture d’écran 2024-05-19 à 23 41 00" src="https://github.com/onizukais/sybil-check/assets/170208261/0d33ae01-2156-44b2-b0f8-d4a352ccf056">
<img width="984" alt="Capture d’écran 2024-05-19 à 23 41 14" src="https://github.com/onizukais/sybil-check/assets/170208261/f5da09d1-6a7d-4c45-9444-eb37e2aabf10">
<img width="980" alt="Capture d’écran 2024-05-19 à 23 41 28" src="https://github.com/onizukais/sybil-check/assets/170208261/f65e9e3b-d360-42d9-a66f-475febdb5525">
<img width="1002" alt="Capture d’écran 2024-05-19 à 23 41 42" src="https://github.com/onizukais/sybil-check/assets/170208261/32a70bc5-d1bf-4b36-bda0-aad221ec1a4b">



These addresses share the same CEX deposit address, are part of a cluster with multiple internal links, and exhibit the same on-chain behavior. This suggests a large-scale sybil operation, likely automated by scripts.


 



CLUSTER 54

The first 9 addresses of the cluster share the same OKX deposit address: 0xE7d9306fbB0e6331E98D8CDf5A63D2c2D9eaA855. The remaining addresses are linked to numerous other addresses within the cluster multiple times.

```
0x7ff630219db6bc7ace11946dce8465f814f0c293
0x8308081db7d66ff56d76d224157a1e1d545aa6d6
0x71075f4e836670e0b6ea7f7834d6f7addd536421
0xa9a4e3a351ace513e9ac3d0df3f9146220bca9ef
0x64ad047d7e1d1077525e7396093e640c159de52c
0xf39a557a1fdb4fd1d03b291259d9f4fa585f9c8c
0xd65b4226a3d72a11297dc332603705b0792d0764
0x3f9d1a094deb889aa46d9aedc5f6a101d92a24ab
0x437130539bcf3155a9f1614e9789697845b83516
0x1adf17f665fbf879c75767ecc87f938abc776682
0x3a5688ba86331c4668fef062ccf4bfd6ad2a0d5d
0x18e6293edf7b32830e7d3452e7ccda0029788a90
0xcb547ec878d93cfefd4be94abe0da9b576f81d85
0x758091a94b7904d982ee5b6d85bae5ae4afde404
0xd81bd5ca852f1caf838795fa0669eb761bfeba71
0xd3047e64519d9826918a6ca997fd9171eddaa0f4
0x10435d35d76a227c67a54342796f707af9571db9
0x609f5678ca2b10aa12e1f7153a39d099b0e7ecc0
0xe5b457317c42e2cf7173c33fc85188fccf75e926
0xf0d7fce7c6e83d704c045162d19669f600b2b5a8
0x9d0e4a7d3de79236528c76ef1f6d95141b4a4dae
0x0fa7d8f0e7e458bbb78aa2a2c6c3627433076724
```


 ![fff](https://github.com/onizukais/sybil-check/assets/170208261/19a54b04-c091-4905-9980-0c17d2f7f38c)




These addresses exhibit the same on-chain activity. 

 

 <img width="1512" alt="Capture d’écran 2024-05-20 à 00 07 57" src="https://github.com/onizukais/sybil-check/assets/170208261/bd3bcdab-cf0d-4a2b-89f8-3e153c0b7db6">
<img width="1512" alt="Capture d’écran 2024-05-20 à 00 08 09" src="https://github.com/onizukais/sybil-check/assets/170208261/952c0424-bda5-4894-a824-383503a1105d">
<img width="1512" alt="Capture d’écran 2024-05-20 à 00 08 23" src="https://github.com/onizukais/sybil-check/assets/170208261/68198d5d-982c-42ff-bcf8-eff0dbd309d6">
<img width="1512" alt="Capture d’écran 2024-05-20 à 00 08 33" src="https://github.com/onizukais/sybil-check/assets/170208261/7b6ea0cb-2d1d-43d1-a33e-000ee0220e85">
<img width="1512" alt="Capture d’écran 2024-05-20 à 00 08 42" src="https://github.com/onizukais/sybil-check/assets/170208261/68baf6ed-0fa8-4804-a4e7-c43b6a628dbd">
<img width="1512" alt="Capture d’écran 2024-05-20 à 00 08 52" src="https://github.com/onizukais/sybil-check/assets/170208261/013461cd-f9f6-4834-8562-a624a22f327a">
<img width="1512" alt="Capture d’écran 2024-05-20 à 00 09 01" src="https://github.com/onizukais/sybil-check/assets/170208261/5ed2814d-e2e1-430b-9d90-69eba00dcc48">
 

For example, their most recent Layer Zero interactions are the same, with the same dapps used at the same time in the same order: Stargate 7/8/9/10/11 months ago. 

<img width="966" alt="Capture d’écran 2024-05-20 à 00 36 05" src="https://github.com/onizukais/sybil-check/assets/170208261/e80b6211-9de9-4ddc-8daa-ef7421b85a67">
<img width="1008" alt="Capture d’écran 2024-05-20 à 00 36 23" src="https://github.com/onizukais/sybil-check/assets/170208261/25e387b3-5671-4fcf-a688-940cce4c51c6">
<img width="941" alt="Capture d’écran 2024-05-20 à 00 36 48" src="https://github.com/onizukais/sybil-check/assets/170208261/4a32e7c7-34ae-4ade-97e0-88fe809d3889">
<img width="977" alt="Capture d’écran 2024-05-20 à 00 37 02" src="https://github.com/onizukais/sybil-check/assets/170208261/52ba90cd-1cc5-4544-a29b-ca56a76fe330">
<img width="953" alt="Capture d’écran 2024-05-20 à 00 37 17" src="https://github.com/onizukais/sybil-check/assets/170208261/5ce9100c-d49f-4e49-bc98-3ea2d73fc6a6">
<img width="950" alt="Capture d’écran 2024-05-20 à 00 37 33" src="https://github.com/onizukais/sybil-check/assets/170208261/51a89a7e-eb09-444f-9ab8-a6ec7a1c39ed">
<img width="954" alt="Capture d’écran 2024-05-20 à 00 37 48" src="https://github.com/onizukais/sybil-check/assets/170208261/c95a8436-ce8e-4503-a2ec-8e42bca6cae0">
<img width="936" alt="Capture d’écran 2024-05-20 à 00 38 02" src="https://github.com/onizukais/sybil-check/assets/170208261/274c783c-fb99-4095-8c13-b4ea72f1aa17">
<img width="966" alt="Capture d’écran 2024-05-20 à 00 38 17" src="https://github.com/onizukais/sybil-check/assets/170208261/16ff2267-ceb8-4ccb-912d-5a24a6d6e663">

All the addresses of the cluster locked similar amount of STG (around 40$ worth) in April 2023 on Stargate Arbitrum

These addresses share the same CEX deposit address, are part of a cluster with multiple internal links, and exhibit the same on-chain behavior. This suggests a large-scale sybil operation, likely automated by scripts.

 

 CLUSTER 63

The first 3 addresses of the cluster share the same Binance deposit address: 0xa4Cae6744968d92216dEFcA390bb74563A9A9A2b. The remaining addresses are linked to numerous other addresses within the cluster multiple times.


```
0xfa8118fec97722451e36e84be84c37dd960a1ef2 
0x885ac62415e534665e80ca205290a3798da91159
0x32e9c9397e6257bce4d9e47cf7e697059f22661c
0xb302560a220d1adcc69c5f8d19279f572555b01b
0x6f1fd6ba42f11799913e6a91b6458ea9cd6887ca
0xd53b399bf34305d1cd665c2b092d787c8a5e45b7
0x4b77909b88acd29d364fa4b3cc8ac9464aa9e32a
0x4c164c5301addb304193146bd350c98a6950f1ae
0x17ea86b6baa237c01cc0af7595c931d6d5442cf9
0xd67d2f08cbc0e3b4cd6db121b5e0c0e5425268a2
0xe66e4b4f43b6c7e7df71c0e325ad6797f3e66b3f
0xd4a7385d50fa958d66d0df590e3204211a6027e0
0xd357a7e5c94f46dfbc3c05033b1ff97926a4e4dc
0xb35a83bda02c2cb5af44a8afc79431f9c11e505c
0x50391a21cd153598bf1460d7d1efc0947e5f8e96
0x7e3f41e32b85799c75327f883362af32a2d3e7e4
0x8cc2c2b764d5a0e76e45af8bd037bd989a16b2c9
0x60940e44372ab21e66e30494c9f09b4e154b5143
0x7ab89e577bce4c35ecd7546f758f1c41f9777ccf
0x6e03f76fb77c3b27a1742bbab1ffa6ab4907ed5b
0x6806f5a7d35f6b31f8cee5799fa7f70571b0d2b6
0x938e3b0e9e70607c50c2629fa434b9a4e5f28421
0x427bd8e086a204e4085c4554cfc48b2ed44e602d
0x5712171abca3743563a4594430b4cfe123711d9e
0xc54c577729bb114c7838fb839a74321c9d04efd1
```


![image](https://github.com/onizukais/sybil-check/assets/170208261/be0fa467-8d4d-47a5-8d0b-ca03e71ebfae)



These addresses exhibit the same on-chain activity. 
For example, their most recent Layer Zero interactions are the same, with the same dapps used at the same time in the same order: Omni X 10 months ago, Stargate 10 months ago and Maverick 10 months ago. 

<img width="1501" alt="Capture d’écran 2024-05-20 à 15 50 56" src="https://github.com/onizukais/sybil-check/assets/170208261/e2b6ada4-ff31-4bd6-98e7-b8945213963b">
<img width="1512" alt="Capture d’écran 2024-05-20 à 15 51 13" src="https://github.com/onizukais/sybil-check/assets/170208261/478de235-9e2b-407f-9bbd-3c638bc50315">
<img width="1512" alt="Capture d’écran 2024-05-20 à 15 51 25" src="https://github.com/onizukais/sybil-check/assets/170208261/303ab72a-7cd8-4201-a38f-65cf45034c6e">
<img width="1512" alt="Capture d’écran 2024-05-20 à 15 51 46" src="https://github.com/onizukais/sybil-check/assets/170208261/e2873cca-d35e-4773-b4d3-2506956bc041">
<img width="1506" alt="Capture d’écran 2024-05-20 à 15 52 00" src="https://github.com/onizukais/sybil-check/assets/170208261/dec54011-1f51-41d6-9b93-9d7d07c256ea">
<img width="1512" alt="Capture d’écran 2024-05-20 à 15 52 16" src="https://github.com/onizukais/sybil-check/assets/170208261/42cda558-a9a9-418a-b5cf-ffc0a1a9c96b">
<img width="1512" alt="Capture d’écran 2024-05-20 à 15 52 27" src="https://github.com/onizukais/sybil-check/assets/170208261/49a38690-bbd6-4063-936a-06ad5878389c">
<img width="1512" alt="Capture d’écran 2024-05-20 à 15 52 37" src="https://github.com/onizukais/sybil-check/assets/170208261/93d8d6d1-3448-4770-a1c4-12c5f268de12">
<img width="1512" alt="Capture d’écran 2024-05-20 à 15 52 50" src="https://github.com/onizukais/sybil-check/assets/170208261/6d568ec2-e500-4df3-beec-ecd1ab7bb6f9">
<img width="1503" alt="Capture d’écran 2024-05-20 à 15 52 59" src="https://github.com/onizukais/sybil-check/assets/170208261/1f9b4935-e3fe-406d-9762-e1577aa9d125">




All the addresses of the cluster locked similar amount of STG (around 55$ worth) in April 2024 on Stargate Avalanche

![ScreenShot Tool -20240520162614](https://github.com/onizukais/sybil-check/assets/170208261/d568d467-6ccc-4f6a-9dc6-7140aad59fd3)
![ScreenShot Tool -20240520162657](https://github.com/onizukais/sybil-check/assets/170208261/a0c2eee9-3f6c-4644-bf75-61290e078a4b)
![ScreenShot Tool -20240520162708](https://github.com/onizukais/sybil-check/assets/170208261/66e7ac79-b422-4a57-a38c-7b4c23648f2c)
![ScreenShot Tool -20240520162724](https://github.com/onizukais/sybil-check/assets/170208261/97c14c03-ef7c-4994-a621-6cab1c682d13)
![ScreenShot Tool -20240520162739](https://github.com/onizukais/sybil-check/assets/170208261/10737571-af5b-45d8-b021-7c32e0d5b2bd)
![ScreenShot Tool -20240520162753](https://github.com/onizukais/sybil-check/assets/170208261/eecd15fc-7007-4753-b549-1b89034e727a)
<img width="1041" alt="Capture d’écran 2024-05-20 à 16 25 14" src="https://github.com/onizukais/sybil-check/assets/170208261/94fcd697-fd1b-43a4-bd37-b6ccb7471b13">

These addresses share the same CEX deposit address, are part of a cluster with multiple internal links, and exhibit the same on-chain behavior. This suggests a large-scale sybil operation, likely automated by scripts.

CLUSTER64

The first 7 addresses of the cluster share the same Binance deposit address: 0xa660f0aC0184bB30DE34DF926b8A925226Ec0348. The remaining addresses are linked to numerous other addresses within the cluster multiple times.

```
0x0df415736be40485c5016f21eeb373fb326a7847
0x126c278e6e446aab2c85f0ce0702e315fc03ea2a
0x033f35a020fbdaa7108bd8e509fd50a88a9915de
0x7eacb0c59cd8d701e7fa36078d37d32271577897
0x8c839369dddc406f08f62ae1ad0cb7032c6b05d1
0x80a92b9dbc1f373f7347eff30c1a872107fc78b8
0x77671737074ec0371b814058773fe2a75acc495d
0x242c8db94a1c2693f9a61a6ff8c875493868e8ab
0x1081ebeabe6a0e691efb90b2035c06f3e5a3daad
0x439c13c47f086edefc4a8ed89191d9cbdcc0447b
0x4c2ac25737836b9fa1b7a85b0fd63173eb44ce31
0xb3731d9c9e9af796b845ba6e3125b9fe1f6fb6ea
0xbda1e5782a1a7587c9dc85f2ce9db87309771293
0x8268bcb386b6a44321b7c0e3e0dd152dcba63a17
0xa71f37ffc493b495a22ffb60c51d1b79416dffdf
0x6e0ecf78b0591ee3fc9d90aed0c2e8bcb34ec94b
0x233e61c23b50f8fc7430390672548a66d9db5408
0x186fa940c9ca5b9401dc4226c801c33f11503926
0xb182d472fbfc8195cf325dc1a8545a90ee92f5f7
0x9277dd7dcb96b91e1711096e86ba84a9ba28f40a
0x011e2c14c24fdac66a77802061d8ea26814e5154
```

![image](https://github.com/onizukais/sybil-check/assets/170208261/f43ba262-4cc8-4831-979e-16200fe44602)

These addresses exhibit the same on-chain activity. 
For example, their most recent Layer Zero interactions are the same, with the same dapps used at the same time in the same order: L2Marathon 2 months ago, Harmony 3 months ago. 


![ScreenShot Tool -20240520163915](https://github.com/onizukais/sybil-check/assets/170208261/08e3e6c3-8d6f-41ff-bb6f-41c204f4e305)
![ScreenShot Tool -20240520163927](https://github.com/onizukais/sybil-check/assets/170208261/890621ea-e000-4ed7-be1e-784441561297)
![ScreenShot Tool -20240520163936](https://github.com/onizukais/sybil-check/assets/170208261/b97784fe-1e01-484d-ae36-e741f687660b)
![ScreenShot Tool -20240520164009](https://github.com/onizukais/sybil-check/assets/170208261/0e870438-1ef2-4a23-a97a-610b6ec25200)
![ScreenShot Tool -20240520164022](https://github.com/onizukais/sybil-check/assets/170208261/fa17ba23-437a-4c10-baa2-9e1cd18b3a53)
![ScreenShot Tool -20240520164027](https://github.com/onizukais/sybil-check/assets/170208261/53ae60e2-3519-4ca5-b413-205df7eb6ae9)
![ScreenShot Tool -20240520164045](https://github.com/onizukais/sybil-check/assets/170208261/55b9da6b-a099-401e-8751-3c93bad88c07)
![ScreenShot Tool -20240520164054](https://github.com/onizukais/sybil-check/assets/170208261/d7f55c38-7c82-4c3a-be77-9e65d60589e3)
![ScreenShot Tool -20240520164101](https://github.com/onizukais/sybil-check/assets/170208261/7f521e4c-1015-45a7-8a51-c668bc16b081)


These addresses share the same CEX deposit address, are part of a cluster with multiple internal links, and exhibit the same on-chain behavior. This suggests a large-scale sybil operation, likely automated by scripts.










CLUSTER71

The first 9 addresses of the cluster share the same OKX deposit address: 0xc0df049ae853686B06D7bF96d0977bd1D249BA6b. The remaining addresses are linked to numerous other addresses within the cluster multiple times.



```
0x2b30a4330f325412fa95b47b95b08c23ae6f5ac3
0x75fe6eacc70f8849343f50e7456ae30f8916049d
0xb89d39dca076c6db5e32f8baca14be07b7587081
0x97c69a36dcf5600e4a0167e872b9e40272a53a8a
0x6b5aabaed263c92d32075df3b9f51c5f37fbfe68
0xec4424496c6fc6edc9984dbeb45e05dd5c847421
0xaf9935c3aeac23f4df59fd6cd2ca004e1833c658
0xf0b6aab4609cf2e3960498fcf2c4a1f70ac52b6e
0x761497cf1f3f3ad8297dee6eb437f56d7951a495
0x03529c232732fa4cc057a923cf48d375d7b0f2ca
0x7604343259f0702a530ea2ebd7496f08c697a93c
0x1160aee5ef827127b24ca5c9d836c4905d98b7a3
0xd70d7edf6248a00166e610f078706cad1104be2a
0xbcefc8761d6589a887110a0d16e46f6a9dddf6f4
0xe250daf80b585ae4b429a56070d3a6592e629f3b
0xae45597fe20430b56a72b0169f7e5bd1d89598b4
0x18e42d83dedcb4de2c5c2cd60e703205be0a02e2
0xb935b780b4eca31129b90cf378f4499caca73854
0xab23618dd560fc4e63d0d55cc3d1e0f562cc0be7
0x2297201990f7d27c27731cffa36602fabc2d1c42
0x378264946dffc32049855ecaf1f77516ee6d94a7
```



![image](https://github.com/onizukais/sybil-check/assets/170208261/8a0d4074-ad9e-4b5c-8326-ef3029ac33b7)

These addresses exhibit the same on-chain activity. 
For example, their most recent Layer Zero interactions are the same, with the same dapps used at the same time in the same order: Stargate 3 and 6 months ago, BTC.b 5 and 10 months ago. 

![ScreenShot Tool -20240520182521](https://github.com/onizukais/sybil-check/assets/170208261/9a6f85f2-f7a6-4052-b277-1707c824b166)
![ScreenShot Tool -20240520182530](https://github.com/onizukais/sybil-check/assets/170208261/ff0381c6-5325-4317-90fa-17b0eb778bda)
![ScreenShot Tool -20240520182536](https://github.com/onizukais/sybil-check/assets/170208261/17172000-bd00-4138-8471-e22bfe0a1926)
![ScreenShot Tool -20240520182544](https://github.com/onizukais/sybil-check/assets/170208261/4cdda94c-17a7-4c09-bc36-d62e956746e3)
![ScreenShot Tool -20240520182553](https://github.com/onizukais/sybil-check/assets/170208261/489973e3-fa30-437a-b6f1-dfd240438069)
![ScreenShot Tool -20240520182604](https://github.com/onizukais/sybil-check/assets/170208261/8fc3cfcd-dc3e-47a0-9ba3-763452090621)
![ScreenShot Tool -20240520182611](https://github.com/onizukais/sybil-check/assets/170208261/2fa18019-ee32-4250-bd90-11a58b0c8146)
![ScreenShot Tool -20240520182616](https://github.com/onizukais/sybil-check/assets/170208261/2acd04fc-3776-489b-8f03-0fb016b23b4a)
![ScreenShot Tool -20240520182620](https://github.com/onizukais/sybil-check/assets/170208261/c5fa93b0-5dd3-4ded-a1f9-28f543739108)


These addresses share the same CEX deposit address, are part of a cluster with multiple internal links, and exhibit the same on-chain behavior. This suggests a large-scale sybil operation, likely automated by scripts.


CLUSTER108

The first 8 addresses of the cluster share the same Binance deposit address: 0x29d9BA99ad344cCEddb5B8AE47C4fABF19aCd4c6. The remaining addresses are linked to numerous other addresses within the cluster multiple times.



```
0x8af9d879d81598ba375becd38070efdaac447fa9
0x2560d358b94794c5f0ab0a61cd2e68a758bee7c3
0xbcf6ddc21f32602f77c41cf988e2b8632c10c607
0xd7da9095821f508d52a0fe204fdb5814c36a30f2
0x8b2fc02162e8ac212882559e1d4bf89820ffc58c
0xaa96659557b27816661db781f82c7f4b4c13866e
0x1f0fd43158f978ff8c04d655c0aa244834e00cfd
0x22285e35b556dc7705659c2855c8aefc0c58be87
0x9b8f4714844dc8193c20ae838763cc589dc40f39
0xec98a23aec9fc6d5289256cd224b8ff17038493b
0xdd45ce72da2e2cfefb4e9df9f6b908caa18d6110
0xcec8dce8e5a2e5a4ddd8a9c78c5d31efb5338d03
0x350c76ba48ff3f448bfa37f3d8ed6953dc7fabf5
0xc6e6968a2fc3bb40975d8fa83c250724dd7ecbbb
0x7eb2b5fd686bbf691033a58af6338fe15146150f
0x88e40d257bff22047c85efe47c96c1a6965ee557
0x80c05258bd76dad66e23b556919bbf78840c2a86
0x4605415671854387018282ca2909a8f2a845721d
0x84d0811ed9b18a378b108784a3c23092f6dd6c10
0x4d5a5b375f6adfade95d7b78a7920017439549eb
0xf158269e837a3c8f6463ee366c437b524ee1e62b
0x5f242d5d468ed69341a2b14c6f0c22a2f3c03f3b
```


![image](https://github.com/onizukais/sybil-check/assets/170208261/39110095-4756-4577-987b-4a763da6c0ff)




These addresses exhibit the same on-chain activity. 
For example, their most recent Layer Zero interactions are the same, with the same dapps used at the same time in the same order: Stargate 3 days ago, Superform 3 days ago, Testnet Bridge 25 days ago and Aptos Bridge 28 days ago. 


![ScreenShot Tool -20240520190619](https://github.com/onizukais/sybil-check/assets/170208261/b52a8ae0-8b28-48e8-93bb-1002c32f4859)
![ScreenShot Tool -20240520190628](https://github.com/onizukais/sybil-check/assets/170208261/4f12aedc-5aeb-4a13-b95b-60671f4b463a)
![ScreenShot Tool -20240520190637](https://github.com/onizukais/sybil-check/assets/170208261/7904fcb0-ad69-4bb6-93ea-bc226facca59)
![ScreenShot Tool -20240520190643](https://github.com/onizukais/sybil-check/assets/170208261/0486a8a1-6185-4cb3-aa57-c57c1685a6a1)
![ScreenShot Tool -20240520190651](https://github.com/onizukais/sybil-check/assets/170208261/76c859f3-1b0d-47eb-8a2d-297e45c9697e)
![ScreenShot Tool -20240520190700](https://github.com/onizukais/sybil-check/assets/170208261/049d16e1-9e2c-4f28-bd79-1f7b9ccff847)
![ScreenShot Tool -20240520190711](https://github.com/onizukais/sybil-check/assets/170208261/e452fa7b-3d7e-4efb-a35c-efdaafc4bf43)
![ScreenShot Tool -20240520190719](https://github.com/onizukais/sybil-check/assets/170208261/f4644849-061f-413b-8fcf-519bb57c9667)
![ScreenShot Tool -20240520190725](https://github.com/onizukais/sybil-check/assets/170208261/0409787e-f509-4658-b6ea-18147b5b8e39)
![ScreenShot Tool -20240520190731](https://github.com/onizukais/sybil-check/assets/170208261/06f3ae96-ebbd-4c2c-b96a-6870e5dddc3b)


Then, we can notice that these wallets made the same bridge transaction on Orderly Bridge, for the same amount (around 100$), at the same date period.

![ScreenShot Tool -20240520191911](https://github.com/onizukais/sybil-check/assets/170208261/1415766e-73e5-4564-94b2-64dc519b7923)
![ScreenShot Tool -20240520191932](https://github.com/onizukais/sybil-check/assets/170208261/bbf16233-8b3a-4bd5-839c-890aceb09eb4)
![ScreenShot Tool -20240520191946](https://github.com/onizukais/sybil-check/assets/170208261/71f3008f-561f-41a7-bfe6-02db67eaa197)
![ScreenShot Tool -20240520192002](https://github.com/onizukais/sybil-check/assets/170208261/4cfe2aa4-9b7f-44dc-863e-2082d6d5f201)
![ScreenShot Tool -20240520192017](https://github.com/onizukais/sybil-check/assets/170208261/fe6dabee-02d8-4b02-bbd9-336bc89a771c)
![ScreenShot Tool -20240520192030](https://github.com/onizukais/sybil-check/assets/170208261/d859672b-8a6e-4ced-8223-edc360533d25)
![ScreenShot Tool -20240520192046](https://github.com/onizukais/sybil-check/assets/170208261/f20d56e0-4fd5-471a-b6c5-64d90cb46ab6)
![ScreenShot Tool -20240520192102](https://github.com/onizukais/sybil-check/assets/170208261/454d448c-aace-4f5f-87fc-66d1f4eb6559)
![ScreenShot Tool -20240520192117](https://github.com/onizukais/sybil-check/assets/170208261/aa54eaff-c271-462b-8c74-c84b335f2686)
![ScreenShot Tool -20240520192128](https://github.com/onizukais/sybil-check/assets/170208261/e2b64a7d-a46f-4abc-8e8c-71993fd4e81a)



These addresses share the same CEX deposit address, are part of a cluster with multiple internal links, and exhibit the same on-chain behavior. This suggests a large-scale sybil operation, likely automated by scripts.



CLUSTER109

The first 8 addresses of the cluster share the same Binance deposit address: 0x2Bda48f4002F6cC364696e990F267A0c5b25054E. The remaining addresses are linked to numerous other addresses within the cluster multiple times.



```
0xf4485a311080369cfc22a1c8d90141355374f3a5
0x0d8141fe30928e85f50e8fbc0acec2595538963b
0x0283d8ca73f07c57937980428fcb7596350bd68a
0x9dae62c6df19b8f31eb9fe15eb5d4e85049262a5
0x01ac8fcbfb857292928f0a5f472e5e0e8fb3d4f6
0x4effa9c9b1c7a5cd11b37f28c1335a8c7638dced
0x74db9c95a291d84de8d9b354ef129668132cf815
0x0d99d6d50701cca22ca67ad07fa126e4da6fd8ff
0x0f11156dd845695655ccd49c157c98f1e2ddbeae
0x040beae0db0e1c63c93c8a09c82e523f585f9e1e
0x4e4fdd691ba1799fc201ea6fae18c687ef56b676
0xe12191218bd45324ed14761aa510b44850e9a056
0xfdc3b2b1a32685cd30a63a21506c70d73550324a
0x86bfa457b54c6c5d12e120a7fe0485d2ab8a03f2
0xb10a9702967d14c5d1a1f0a281284b3c7ce78acb
0x3a94614da0494018401489ec3a85da2d1b66bb54
0xe082de18106d0dad1a04d940edb9a511e29476dd
0xcaa8de126d06b3aa908a59aa717a257deaa6354f
0xc02c950c8aadfc16f58457af469d3d99ed77ed59
0x0c28527d42c3224b6588f84f28e05406b93c079b
0x427c162ee27920080829bf1ae010b260fe1e3677
0xf4c10b941715f7ade7c37e14cce743330939a9b1
0x4f687d4aa13143cb81f48018bd2f956ebfc6ca41
0xa2ab59f0fcb3d280bd89fe472f573b0e403dcab5
0x81087a9d507fd0e9cf92877f6a3143a4920a9b20
0xf85b00d368643b2fbc8b0c3f55f2de7a00437c10
```

![image](https://github.com/onizukais/sybil-check/assets/170208261/b8e65238-63c6-4fb7-903a-4b755ccb5856)


These addresses exhibit the same on-chain activity. 
For example, their most recent Layer Zero interactions are the same, with the same dapps used at the same time in the same order: Stargate 2 months ago and Merkly 2/3/4/5 months ago. 



![ScreenShot Tool -20240521000011](https://github.com/onizukais/sybil-check/assets/170208261/5afc6d47-95c8-4fcb-a480-39c7b8144060)
![ScreenShot Tool -20240521000016](https://github.com/onizukais/sybil-check/assets/170208261/f8289a7f-5a58-43bd-9acb-21c4e750f43c)
![ScreenShot Tool -20240521000019](https://github.com/onizukais/sybil-check/assets/170208261/34b020a6-07bb-43e3-8f22-0bce6e8bda00)
![ScreenShot Tool -20240521000024](https://github.com/onizukais/sybil-check/assets/170208261/4927629d-e2c6-4a1e-ba2e-dda88d1d6266)
![ScreenShot Tool -20240521000036](https://github.com/onizukais/sybil-check/assets/170208261/6a625ce1-23f9-46d2-90b4-948c287461cc)
![ScreenShot Tool -20240521000050](https://github.com/onizukais/sybil-check/assets/170208261/3b39da4b-4701-4769-a13a-f269cd0917ea)
![ScreenShot Tool -20240521000102](https://github.com/onizukais/sybil-check/assets/170208261/11b95c2d-1dca-43cb-8501-8fb4b8646d01)
![ScreenShot Tool -20240521000108](https://github.com/onizukais/sybil-check/assets/170208261/0c1c9eb5-3007-4d6e-843a-9f672f2484a9)
![ScreenShot Tool -20240521000123](https://github.com/onizukais/sybil-check/assets/170208261/3eb1c1b9-a9d8-41b1-ad80-986cbc554f4a)

All the addresses of the cluster locked similar amount of STG (around 5 $STG) on the same date range in May 2023 on Stargate Polygon and Stargate BSC.



![ScreenShot Tool -20240521001521](https://github.com/onizukais/sybil-check/assets/170208261/db4c5e09-7bf2-49e9-a788-58e49e942ddc)
![ScreenShot Tool -20240521001542](https://github.com/onizukais/sybil-check/assets/170208261/0ed4153c-a076-4136-8707-019bd8705840)
![ScreenShot Tool -20240521001557](https://github.com/onizukais/sybil-check/assets/170208261/87348131-aa98-49b4-9a01-2c390cb187dd)
![ScreenShot Tool -20240521001614](https://github.com/onizukais/sybil-check/assets/170208261/78fcb32f-902c-492f-873e-ccffc5618e41)
![ScreenShot Tool -20240521001627](https://github.com/onizukais/sybil-check/assets/170208261/5d3f232b-c5a6-4763-8fe0-34c390bee249)
![ScreenShot Tool -20240521001648](https://github.com/onizukais/sybil-check/assets/170208261/959ff4a5-9d06-4926-85b8-8e526867c205)
![ScreenShot Tool -20240521001708](https://github.com/onizukais/sybil-check/assets/170208261/5b2097f2-7a82-48fc-92cd-2ad0c3e8ae19)
![ScreenShot Tool -20240521001724](https://github.com/onizukais/sybil-check/assets/170208261/f7248243-03f2-43f5-9c24-fb2d058192ca)
![ScreenShot Tool -20240521001736](https://github.com/onizukais/sybil-check/assets/170208261/a7ebb129-b761-4270-8b92-4d7229ba92b1)
![ScreenShot Tool -20240521001748](https://github.com/onizukais/sybil-check/assets/170208261/10b4f3fa-ace0-4e41-9208-3bcf1e95018e)




These addresses share the same CEX deposit address, are part of a cluster with multiple internal links, and exhibit the same on-chain behavior. This suggests a large-scale sybil operation, likely automated by scripts.

CLUSTER119

The first 8 addresses of the cluster share the same OKX deposit address: 0x40Cee519D40f47BA6f0c57bEE874377BFe366eBA. The remaining addresses are linked to numerous other addresses within the cluster multiple times.


```
0xf6b2c339304b4e3f37a73b5e0caba126958ac46e
0x94bf9b83d417b876ae929323d803b67c2a30102c
0x388b165eccf64abac50043280517a905e5f93c7d
0xb4df81934b43890ed759b0151c1dcabd6375643c
0x3b781c73e3d7d3c59781e08933a19ecd5e61eac3
0x82715ec383b5ef8c7e7fb3f1ca079d52a957cdab
0xccbef52f7f777b3cb86d1318e15f4b9cebcae154
0x6f8ce26fd34e21e428fc2cf6cd8ca5ca1520a2ba
0x02c57a67b4a04066f1029d1af807ecebbc09e78a
0x72df54f3db8feedb05b0b59e4eb8f190db832726
0x3c7e24fc436ca1d5fd1c867154b9e5d649d9c2e1
0x882790d69985292647854f43b9e75c38c07cfd8d
0x43aae724f2c111de2d7abc7a9be8044ce9f5445c
0xe8e3a64631fc1b3e3670eb76870cfcfb643303b3
0x523bf62fb4b77a8ec69bc58002c95925aeba4f58
0x394799aa278839f247b42fab10d9d8b92745f288
0x64ef733529ad489c2078b95a1289988a6f4a961e
0xf45fcb6571ea9fe3f102f650feb514e988d2590a
0x361a0069fd2a54f8ad8926a6b8a77212ec70e0a3
0x3a60cd4609d4b0ce6c09a52874fdd9ee7ac55393
0x35c1582f701071bce896ad7a756c5a6da22be4ae
0xc2c4acbe8651bb56c057ad2b6f4edf692820bf77
0xc88fe32236d7611ad75a79ea0114b01e2ec3ed64
0x358de7ff0fef45b77e9effa288022c366348092e
0xe60173109c946c76abd4c8201fbff61377471d10
0x66f077214bd25fcae71293790f30d5ea6edc89e7
0xce8361eb0f1f3d4c45988571ef5d5d39752b878d
0xa63dfda1c5ca12cd586e2e4cdb9a48ac73621f53
0xc5bad3fc9d9f93cdcbb840d7255cdb0c7bdbfed8
0x08b2ddb67abe415b1b9027c24012464095ff338b
0xe81ea44d9bd78383f561076d707ad2b8294bda5f
0x8bb10bb093fe9de5df5e73647583b331f22e0f92
0xc8d4f855fe4a3d88e77ae4eb0bb8be492aeeaf44
0xb044c6e53b0953fe9aa54af1502150a7676fdf47
0x51cecc4035291e7a11e7e4c83997b6677d1384c7
0xc8e859ba302b49ede550d60b5546a1db93220376
0x415b0d6545690c9a06e9b461e3cf1d699826a9e7
0x1b5b5f524af8978fc67bfc2fbb8ad94e51e7e9e5
0x7c1653afa616d317035b7e25b67e57e31085c218
```



![image](https://github.com/onizukais/sybil-check/assets/170208261/e0a4b5ed-f9f7-406a-9174-874e6cfbebf7)


These addresses exhibit the same on-chain activity. 
For example, their most recent Layer Zero interactions are the same, with the same dapps used at the same time in the same order: Stargate 2 months ago, Merkly 2 months ago and Aptos Bridge 2 months ago.

![ScreenShot Tool -20240521003843](https://github.com/onizukais/sybil-check/assets/170208261/0983d2f6-0747-4774-8ee5-46e6d4d51a15)
![ScreenShot Tool -20240521003846](https://github.com/onizukais/sybil-check/assets/170208261/9afc92cc-3a5d-4bad-bd48-d0bff8d92788)
![ScreenShot Tool -20240521003854](https://github.com/onizukais/sybil-check/assets/170208261/6b6bc5eb-745f-4600-9920-2ddfcbd28569)
![ScreenShot Tool -20240521003901](https://github.com/onizukais/sybil-check/assets/170208261/6ed9bacc-593b-4bb7-9cd3-9c85d7b54d47)
![ScreenShot Tool -20240521003906](https://github.com/onizukais/sybil-check/assets/170208261/28b077a5-c60f-42ba-afde-ac87038d432b)
![ScreenShot Tool -20240521003912](https://github.com/onizukais/sybil-check/assets/170208261/9c182b00-c3bb-48b3-b372-fce232fdc89c)
![ScreenShot Tool -20240521003920](https://github.com/onizukais/sybil-check/assets/170208261/c669e562-17a7-4bd1-a25b-eb370fe71fb6)
![ScreenShot Tool -20240521003932](https://github.com/onizukais/sybil-check/assets/170208261/3cc67a97-0468-4c75-9778-261849831ac4)

All the addresses of the cluster locked similar amount of STG (around 40 $STG) on the same date range in March 2023 on Stargate Optimism.

![ScreenShot Tool -20240521021824](https://github.com/onizukais/sybil-check/assets/170208261/aec8c27d-6fb9-40cc-b623-5c72d798cd09)
![ScreenShot Tool -20240521021858](https://github.com/onizukais/sybil-check/assets/170208261/f25bde72-69b2-47d9-af26-a02f672eb2a4)
![ScreenShot Tool -20240521021928](https://github.com/onizukais/sybil-check/assets/170208261/35f07f26-aedd-4daf-9f93-6fc10e5af83c)
![ScreenShot Tool -20240521021942](https://github.com/onizukais/sybil-check/assets/170208261/2e639985-0e15-473f-bead-ae6177ce7963)
![ScreenShot Tool -20240521022010](https://github.com/onizukais/sybil-check/assets/170208261/f756b68a-f211-4670-950d-8de95036c6ee)
![ScreenShot Tool -20240521022040](https://github.com/onizukais/sybil-check/assets/170208261/dc17a32d-0ad8-461a-a82e-844677c275b4)
![ScreenShot Tool -20240521022103](https://github.com/onizukais/sybil-check/assets/170208261/0d5d18b7-38dc-45d1-a02f-e3cd4545b9c7)
![ScreenShot Tool -20240521022113](https://github.com/onizukais/sybil-check/assets/170208261/7f806672-4779-4a35-95ec-db85d2f12201)


These addresses share the same CEX deposit address, are part of a cluster with multiple internal links, and exhibit the same on-chain behavior. This suggests a large-scale sybil operation, likely automated by scripts.

CLUSTER126


The first 14 addresses of the cluster share the same Binance deposit address: 0x553dCEe501865C6dE9d4d7A3A3011661352006fB. The remaining addresses are linked to numerous other addresses within the cluster multiple times.

```
0xbe1122908803a1a52ab6c6ba1774398249ae93ca
0xe590fa9cbd5fdd8cec05b306d3223418b9c0c246
0xfdd0986b799d135d16a128bcb5ff7da1cee058b2
0xe328b5120378d93cf94c015fc6b6fdb4a2ce6c95
0x9b922e47bad76614aa2e1d8d1faf138d04d9d13c
0x141d4b109304f7a34f7cd6dd0e4691826572d812
0xf41733d952338540b6f1e07480fdbeb3f7919bbd
0x1d2a03031b1edfa54f42081627bb9d48839ea636
0x79cb30bbfe89ccaaf334540a6be48fc0483fd944
0x365f1f8ac36639f3e484a652fe9b21f8c9b5433d
0xa70d36cd8ab6454ff736bd66b3089b3a693ea045
0xe5ccb63a3423cb7055e45cd854911078412c47f2
0xb3ddf8580d55c48c9bf5c7de43e97aa1ce663869
0x9c535947c85754fa686351feae36f480032eee02
0x35d3e27ada40f49af6209c1f2405e136c8a80e35
0x7236fcf927bceadd93d76b705afc7e4763c94290
0xb4a4c0add48618dd3bf02e27c54833e3e0d17630
0xf591d72e6d7657ca587315bac0dfb9130c1e5e7c
0xb3ab6804483ca39a5e0d5ba83661ce3c23c54622
0x4fd1c95153553bdaf46c896dbc01a45fc1825d9c
0xce1d5cf3329b209d7eff54ef2b08e48217e5a300
0x6c831dc0abc1aabd9491969f72832c949b620d71
0x49b1c6f5e583265a01947f28ddeb80c03cdf2dbe
0x54cf4f3a8ccf3a27933e7caf9e5bf5304479c5ec
0x812db8d92e1215729fabad7108395a6a7ac9134a
0xc95bd0c4144df206890c1641d675c3c2c55108c4
0xff78bc9fcf58768acc5fcbbd412ad1fa00e6391a
0x4c0b9ff9a8ef2c53a438171654bfe2fa6a5f873b
0x493b097d4b78b3973de97464ff4284c507674e92
0xb31a089aa8ef4d691348d194e86b5a437ca778e8
0x41e061dea7ea4527db340ece9922698c5943bf98
0xa5caa5a5f1c4c20f8756f36c5b32039d2969ed55
0x863429c69e45c66758f3052f3e4eeb6e0c39f58a
0xe8a675fc62d7abda6e308650afcbf38d7802956b
0xc46b2b4cb2b350cb851fbf09fc14430eb14adc5d
0xf5fd85540d85a7d2b141b6481c7528be686a7208
0xf4ffb5ce30644bd02a32e5980d785630afd1c26b
0xec8909add2e7941566eb19f648e5383d44d85c42
0x937d428e279f7bd013c821a09adfc045b195362d
0xb497ab001dd168fcdfe6e840ffb5928db7eb8f4d
0x670db67da8b197e07006b377950518dbf1b0e59b
0x64d15838038f97d40cd39a6dcbcced03ec58be5f
```


![image](https://github.com/onizukais/sybil-check/assets/170208261/1de57c24-5511-4af3-a3e6-44436438532c)


These addresses exhibit the same on-chain activity. 
For example, their most recent Layer Zero interactions are the same, with the same dapps used at the same time in the same order: Stargate 2/5/7 months ago, Merkly 1/2/5 months ago and Aptos Bridge 2 months ago.

![ScreenShot Tool -20240521031559](https://github.com/onizukais/sybil-check/assets/170208261/4d4f20b7-8406-4e4d-ab19-ae6bdf025316)
![ScreenShot Tool -20240521031602](https://github.com/onizukais/sybil-check/assets/170208261/edae8738-a2ff-4990-8488-645cb86c23b7)
![ScreenShot Tool -20240521031606](https://github.com/onizukais/sybil-check/assets/170208261/c6501dbd-509a-438a-bc00-ccda47d7183d)
![ScreenShot Tool -20240521031609](https://github.com/onizukais/sybil-check/assets/170208261/2ad10f74-456e-40e1-9642-7d8f686660bf)
![ScreenShot Tool -20240521031616](https://github.com/onizukais/sybil-check/assets/170208261/136dccae-cc21-4f44-8f7c-078f7e05121e)
![ScreenShot Tool -20240521031622](https://github.com/onizukais/sybil-check/assets/170208261/3ab585bb-e0d4-491c-868f-21fb96f3e2d4)
![ScreenShot Tool -20240521031629](https://github.com/onizukais/sybil-check/assets/170208261/940b96c5-8503-4cfc-b56d-8f2d03bb0051)
![ScreenShot Tool -20240521031633](https://github.com/onizukais/sybil-check/assets/170208261/59651028-0767-4cda-8780-7e37a5982775)
![ScreenShot Tool -20240521031636](https://github.com/onizukais/sybil-check/assets/170208261/bd4c4634-bb5f-4f1b-b6d0-41baf2cb52f2)




These addresses share the same CEX deposit address, are part of a cluster with multiple internal links, and exhibit the same on-chain behavior. This suggests a large-scale sybil operation, likely automated by scripts.

CLUSTER135

The first 6 addresses of the cluster share the same OKX deposit address: 0x6Ac489A83C5207B052D0A7D7638EE6eDB52afE92. The remaining addresses are linked to numerous other addresses within the cluster multiple times.

```
0xd89765a3e7633fcbb2b9bfcf3c639e4d1653afaa
0x68db90264b5f95032110965e2b4ca7353d67f9f5
0x6fbca37a3d4933f1ec9419a4c3da5d5329cddfc2
0xb339297171670de477002e1e3bd429b87d2da263
0xf34d1ad73660807b15bc379c9b0a723bd0e9e6b9
0x7844ba3f77e1fcf03ed6044eb5496c1f91914134
0x2d232c211c80c8ce716b884b8fcd784bb55e6053
0x50270d3eea45820a33e7b57072e49c37f0fbf40e
0x8d8979ba8c18e0591f08cdefa54980a13b71df1b
0x2caaa9c911de5990b474eb5c7679b8662d931eb2
0xad8a954fab2e71f3865a8272c4042e10d83e3d5f
0x8cb50b46e0708dc0b2b34e6077b876eb95a057af
0xe2709b901d6ea39ffca044679b4e268f65c68661
0xa69bde39bafa75534befd12a5f36ec8f95248009
0x227fbcb2931d501a31f29b1a356e12f71c6deb8d
0x9aa1575e60d33cd8e750f3193bdfa7d5540fe136
0xf59a93cf770eb6e2b4344387ce835c58ff8b363d
0x76fc58dd26ed16baf40a893faef7920afd679036
0xf3f4ee03357483b3b41a1d58b32dc1f57bd29c10
0x4f2dc64360ebbe78c968338ed4baae1d14144340
0x6a643bcc171e12448aa4202db2bfd4b008108a5a
0xdb520b6769df9df5911e5969d570ea12850dac69
0x897aaceb5620805a04b561c076ca49667d663238
```

![image](https://github.com/onizukais/sybil-check/assets/170208261/92b2484c-b035-45da-a116-d65f7d58d591)


These addresses exhibit the same on-chain activity. 
For example, their most recent Layer Zero interactions are the same, with the same dapps used at the same time in the same order: Merkly 20 days ago, Stargate 4 months ago and Merkly 6 months ago.


![ScreenShot Tool -20240521181045](https://github.com/onizukais/sybil-check/assets/170208261/ebc88dc9-31e1-4125-8758-9f1d46f0af5b)
![ScreenShot Tool -20240521181048](https://github.com/onizukais/sybil-check/assets/170208261/4a4df353-6a9b-48c6-8a2e-8fdc444089f6)
![ScreenShot Tool -20240521181052](https://github.com/onizukais/sybil-check/assets/170208261/4ec93757-ddeb-45f5-b69d-28eba84b5530)
![ScreenShot Tool -20240521181057](https://github.com/onizukais/sybil-check/assets/170208261/c563897d-fb03-4773-b32b-0d456596a89c)
![ScreenShot Tool -20240521181104](https://github.com/onizukais/sybil-check/assets/170208261/3ff4346d-0f71-40d4-aed4-8f8577a87ddf)
![ScreenShot Tool -20240521181117](https://github.com/onizukais/sybil-check/assets/170208261/d362e873-f070-4bee-913a-fc8c5e935da4)
![ScreenShot Tool -20240521181122](https://github.com/onizukais/sybil-check/assets/170208261/545bb6b1-c7a3-49f4-809f-76468a75ba5f)
![ScreenShot Tool -20240521181127](https://github.com/onizukais/sybil-check/assets/170208261/0417e2e5-9e20-4f8a-8d0f-f85045f4aa1d)


These addresses made similar deposit on OKEx on the same date range in December 2023.


![ScreenShot Tool -20240521190806](https://github.com/onizukais/sybil-check/assets/170208261/a4cb7caa-f5c1-4ab4-9eca-d1b0a77ae26e)
![ScreenShot Tool -20240521190825](https://github.com/onizukais/sybil-check/assets/170208261/9f1d1cf0-1643-4b35-8a27-705210f58a95)
![ScreenShot Tool -20240521190848](https://github.com/onizukais/sybil-check/assets/170208261/c3716279-9b09-499e-9b3e-e72f3466452f)
![ScreenShot Tool -20240521190859](https://github.com/onizukais/sybil-check/assets/170208261/39d906a5-5088-40bc-a98d-e98f8151cf6e)
![ScreenShot Tool -20240521191003](https://github.com/onizukais/sybil-check/assets/170208261/eb1e0e46-491f-4729-8c52-161be3d27693)
![ScreenShot Tool -20240521191238](https://github.com/onizukais/sybil-check/assets/170208261/45dfa778-7dd6-4712-8d48-3199045dc731)
![ScreenShot Tool -20240521191250](https://github.com/onizukais/sybil-check/assets/170208261/9a0621ad-aa1e-4ed6-a084-f4c175b6763d)



These addresses share the same CEX deposit address, are part of a cluster with multiple internal links, and exhibit the same on-chain behavior. This suggests a large-scale sybil operation, likely automated by scripts.






CLUSTER5

The first 7 addresses of the cluster share the same Binance deposit address: 0x7D8470F46E49455070874c306d7C3601e30fa46e. The remaining addresses are linked to numerous other addresses within the cluster multiple times.


```
0x3706eeb4837bb5bb5b203f5e6f8531e4eb565d9c
0x537ee6247bc659d4eb8a95b0db148769028e37d9
0x3e67fe015ad1c25b841bdf085336c21b53e8cdbb
0xfbdf0dd6d6093b6abe521a1b9f26ea611dbfb6fa
0xa15543dbe851dc015095f02b00c1f414bd365f6a
0x0862b872d63d399c16513a27bf63f683900b988f
0x76fd51e103181954e244c7c2b23e499b14932ed7
0xc488563b3aa121f4b296ce56fde01ef256b0c440
0x3807a4fd8ed467d21c577a833868c4ad03dc21c2
0x430cff5356fdbad334e8c992e5be56bed769b0ce
0x6d4f5f9511c3648fdc869170480640c15a20c09a
0xef6512fa4c965784449d2f9fcd89de1f3d66c917
0xf2a2a2c5bb1aaaa11b7bb2863d881296910299bd
0x2cc43761ae77a6db65ef6ab84badf983249893d2
0x3768cba9ce338c79d99142524b2bf337aa385663
0x3a0e1e04aec0c8ded8e7820952e78c680f0ff2c6
0xa51f88df549bcede2cacb4a37ec4dae4328af48e
0xa44c591e28a235337df35f33fcfff9fa803bda80
0xb7a5a54c3ac341da34b2b21921c6f6f56410ab09
0xeacafa6dc551d5e27548f7edc2a1d9f5ed4269f9
0x553c56d0a9401370bc9b552add75a09b0bb0dccc
0xa042a3c58f60e1bb3d7e45b4b588e46a9f54377c
0x58d0d9c1270a0be6abc950f593bdb10edd731b00
0xee4a6bda90c43ceeb7cf49fecb710ffe1b405997
0x7e342ca8dc1b9c839006704f1b61be87fb5fe9a6
0xca6681620716414bbd33c05b6ca48d8827891774
0x99b48b027b3a121aa01fcc692cca19b26fede758
0xa33d99ae94fe642c410013f50de978fc114888de
0x3ceaa9cf33902a1e2ec99b6a76ab914c1caf4b75
0xb593d71183c9df32b9cf8be12fde90e27dcfd7f9
0x33367d072d33d9653874b545f7da707527b1a3c0
0xc8930433a67e6cbeeeb699c5e02055ea832d39d2
0x38455642dc72a11f4645ded27353bc97a5054192
```

![image](https://github.com/onizukais/sybil-check/assets/170208261/b029945f-f10c-41c7-982f-784f28b84210)


These addresses exhibit the same on-chain activity. 
For example, their most recent Layer Zero interactions are the same, with the same dapps used at the same time in the same order: Harmony 3 months ago, Abracadabra Money 3 months ago and Merkly 3 months ago.



![ScreenShot Tool -20240521200802](https://github.com/onizukais/sybil-check/assets/170208261/066bf15c-2e53-4c8c-8be7-b1e9fef1b20e)
![ScreenShot Tool -20240521200805](https://github.com/onizukais/sybil-check/assets/170208261/689d4022-8bca-4305-b165-750f12cc7fcc)
![ScreenShot Tool -20240521200808](https://github.com/onizukais/sybil-check/assets/170208261/0454c626-f1b1-48ce-9061-392020b989cb)
![ScreenShot Tool -20240521200813](https://github.com/onizukais/sybil-check/assets/170208261/7167a965-635d-4d0e-8064-024ee1d4c2ba)
![ScreenShot Tool -20240521200816](https://github.com/onizukais/sybil-check/assets/170208261/0f55aae5-f0b3-450c-b52d-40a76253f130)
![ScreenShot Tool -20240521200822](https://github.com/onizukais/sybil-check/assets/170208261/c960402f-c752-4d48-83bf-9030ce27aa06)
![ScreenShot Tool -20240521200825](https://github.com/onizukais/sybil-check/assets/170208261/1d305c54-2c95-4e68-b19e-714df718c76e)
![ScreenShot Tool -20240521200827](https://github.com/onizukais/sybil-check/assets/170208261/e0e15e35-5e81-4e15-b063-aaba570b4c57)
![ScreenShot Tool -20240521200830](https://github.com/onizukais/sybil-check/assets/170208261/ec4d6373-2aef-493d-8bfe-da766c942fc1)



All the addresses of the cluster locked similar amount of STG (around 30 $STG) on the same date range in April 2023 on Stargate Arbitrum.



![ScreenShot Tool -20240521203729](https://github.com/onizukais/sybil-check/assets/170208261/91f14303-2f20-4d68-a268-507f67bc81a2)
![ScreenShot Tool -20240521203738](https://github.com/onizukais/sybil-check/assets/170208261/22043fe7-73f9-4c66-b40c-256d1b09e622)
![ScreenShot Tool -20240521203748](https://github.com/onizukais/sybil-check/assets/170208261/ac6ff209-5534-4262-9916-1fa67635fbbb)
![ScreenShot Tool -20240521203808](https://github.com/onizukais/sybil-check/assets/170208261/5cb76dae-6503-4975-8841-01c87d571385)
![ScreenShot Tool -20240521203828](https://github.com/onizukais/sybil-check/assets/170208261/5efd822a-0827-4c4f-80c8-cfcc4841444a)
![ScreenShot Tool -20240521203842](https://github.com/onizukais/sybil-check/assets/170208261/784f723e-a9d0-44aa-8c2a-25d6d3aafef2)
![ScreenShot Tool -20240521204048](https://github.com/onizukais/sybil-check/assets/170208261/9298e1a0-744d-47c8-b79e-4c384b848d0e)
![ScreenShot Tool -20240521204101](https://github.com/onizukais/sybil-check/assets/170208261/42657d2c-25a5-4094-b6c4-373f42c3f0ac)
![ScreenShot Tool -20240521204113](https://github.com/onizukais/sybil-check/assets/170208261/81566146-d451-4690-a412-9e6fe82901cb)


These addresses share the same CEX deposit address, are part of a cluster with multiple internal links, and exhibit the same on-chain behavior. This suggests a large-scale sybil operation, likely automated by scripts.


CLUSTER124

The first 9 addresses of the cluster share the same Bybit deposit address: 0x54ECe100579a991fB08A0a8DA9c0367466cd2E96. The remaining addresses are linked to numerous other addresses within the cluster multiple times.


```
0xa7caea9576e11eb2fd793b92d02cf467ffbf48ec 0x842d0a47cf5b661adeb2e5a3e1afb61ae0a27423 0x44e688025ec441fa43856bd5516368dda8ad1afb 0xd51df14b9d9807b5a06d7699643832bec5395fd4 0x6babf8a88741f75eb09e3a81fa61bf6dcc507f35 0x45c785e38c1a2ec21523b0a27ecffdafea53dfb8 0xb35586ba93aa5dc3c639c940a52b735f7629f976 0x0fa9414c36467d765e47bd85fff94bd7250ca71e 0x6bfe00a4813fa93134a40433d7d974a65fbd6b47 0xa866ccd10e6684a45ec2c31ac38d2f327577cd2d 0x231c5d2490a7c35931bdbd521b1c63d457739906
0xf56aecd5dfd37179203f23581b052190ba8715b1 0xc4ac310e8c9d35a5a693bbc2d626913a542c4dc0 0x08f0a7e08df3a0a35a50d60db353e619219677f0 0xb7ed0f322d8cd453332666747da7b1166049cf12 0xfaf69ccb6b7f6d73b700fc17ed525e277ce41d04 0x4091161bf56129d9caf22d12f589e31d91cfa843 0xafb0a803cbab4e3052cf6f56898d5a8823f776a0 0x4699842934bf5a06ff0f266339a2b040f4ec0d1b 0x963b0cc64c6bd1c79f28a0e12983709d8411776e 0x14828b62edac62de305d90167e315b5dc4c1850c 0xfb288fb673a4a4fbcda7baad1f57b5e5d621ce87 0xe9d091eed6901f97bc7d197e160af23e8ff26dd1 0x558289b335a6ef7e8d63cd164d0c08a4e26bce75 0x666800791cf446e5727ccba6232a2591ebcbfc85 0xf84a165e4ecbe6885e68d3aa3e0b29b553bafe72 0xdb4d9d47c37c41b0604722937c13b39e9758bf6a 0xcbc8b4ccbc04bba60fc4b9c42eb726ec5fdd6f19 0xceb9c2c86cdbbe89f62f8b9cbc24da4c1ec89183 0x63d52ac2af02effe0c83ccd1227ed9a8b849e017 0x48f3bd7ec98d6e46935332162465e4b7fe2630ff 0xcd7773b7d2e564688ab1de1ffed20537e90ae461 0x115b5e5227e07c942f151ce5761ef639723035f2
0x72f0fcf570a51e17396f8a5693c785856f0d6fe4 0x4f6cd5a1e515081200023f419aaaef08a59ea2f4 0x80848cb4b22aa578b4318daab79a57c7fd3b8369 0x5443f2c7f400e97df86a78ab9119d5de31583e1f 0xb1c0ad4906177e697f4b6db1ae90fe14762edf27 0xc3f60c7775f02d799769205294a0c4fc2c4b21dd 0x210c10cb34f8ea80543ae7fd2222ccee130e76d0 0x1e5bfea69f3ea01cf46554c1ff2e595d06b619d7 0x572f86961baac8160a70e232e4c619638754f085
0x3beb9186655a2fbdba170369f79ce3515abc3a12 0xa3e51807c72e98705fdffc47b54d7bffdc13e621 0x4e9429b070b3069db491ebeab217ca82c975d5a2 0x5cfac1a75050b48db1c59c88882c60b82001516d 0x17a44dc7fcf5ac4fee6f86b42c646c429a60b7c3 0xae06244ddd7103e511ad35d47371ff7c0d9fc7fc 0x3895c0a0f9d3b8cb45d3e38d01a40db510a5fb27 0x7876e3f8bf09193080685ef17c2ae02536a61572
0x017b7f32cd06ce39587250bc4c22c4ec918a807e
0x96caedcb12834ac794744445a9e629f5bb3f0dfd 0xdb34f9d155699c5d0c06a9919132b4b3782cc9c4 0xf56270aabdc648e05b0fdc3e93ed05a20c088148 0x61ac400ded9f7f391539e66a9d88c74aa06f0e6b 0x8859ac3d3d26055a8f6c6215c43e12073d850722
0x70ad3e021b88b3b6acd287823be38f2adfd4f6bb 0x14028fb951e900ef4a6910c6ae91cb146f824456 0x65cab4725660bc0980446cc7e7cba64547436b60 0x11ae3354630cf9b74797529a5a78de3910c03239
0xe967e74e323a37ffd327abf2f4d65176e1b11759 0x02d77cf588e781b7f7bcca221401a32a282d22ba 0xbfd071b02657b2b625d30d917bcfdd2bd665f307 0xb872064a42532f43a825e504ce4184f3971b673b
0x3dad69ecb0338f3b5d0ae41f5d8315f7ec73e1b0 0x1825f92a938106870f8e259191b466c4261a2d7e
0xce8ebb4e36bdd0fa84fbccad0a5e4d2caa52d60c 0xf17ef0a5841001838be37906071c5ef40110d666
0x53ea81ea4f82367a5506474e85479fd6d4b5b53e 0x0f94c5152194d02f81784f46d396c367dabdc972
```

<img width="152" alt="image" src="https://github.com/onizukais/sybil-check/assets/170208261/29fb87f8-94d3-440b-a503-fd090682cd1c">

The addresses have the same on-chain activity. Their L0 interaction are the exact same, the same DAPPS in the same order in the same timespan. For example, their latest L0 interaction all are the same, and follow the exact same pattern : CoreDAO 11 months ago, CoreDAO 12 months ago, Stargate 12 months ago and Testnet 1 year ago. This is the result of a script.


<img width="287" alt="image" src="https://github.com/onizukais/sybil-check/assets/170208261/defdc27c-1a44-4daa-b29b-e0cb1f541dbc">
<img width="320" alt="image" src="https://github.com/onizukais/sybil-check/assets/170208261/64da50e0-af0a-4546-8a30-bf9780e987cb">
<img width="329" alt="image" src="https://github.com/onizukais/sybil-check/assets/170208261/be23a816-2534-47b8-b6f6-741e896b35f2">
<img width="340" alt="image" src="https://github.com/onizukais/sybil-check/assets/170208261/c2f4e159-b5fe-4eb4-9eb3-ffdbb58e1e41">

These addresses share the same CEX deposit address, are part of a cluster with multiple internal links, and exhibit the same on-chain behavior. This suggests a large-scale sybil operation, likely automated by scripts. 



CLUSTER200

The first 9 addresses of the cluster share the same OKX deposit address: 0x06897581C555C3746ad4E64ceb4155e31C779E45. The remaining addresses are linked to numerous other addresses within the cluster multiple times.

```
0x50c1430c0c8bebaa2bcbc617106bff63bd7a9a76 0x45b0c219918c42f0ca946bdb91b517275a8c9cca 0x8d8979ba8c18e0591f08cdefa54980a13b71df1b 0xf3f4ee03357483b3b41a1d58b32dc1f57bd29c10 0xd19c0896e7e956e8877d8925e1cf6eebf1f0be41 0x7c48825e342b2017cbd964283a8d1072c8dcf7ae 0xb339297171670de477002e1e3bd429b87d2da263
0xe895909b9cc3000ae3e6008ede594b9f7f0f870b 0x2caaa9c911de5990b474eb5c7679b8662d931eb2 0x2d232c211c80c8ce716b884b8fcd784bb55e6053 0xad8a954fab2e71f3865a8272c4042e10d83e3d5f 0xf59a93cf770eb6e2b4344387ce835c58ff8b363d 0x8cb50b46e0708dc0b2b34e6077b876eb95a057af 0x4f2dc64360ebbe78c968338ed4baae1d14144340 0x50270d3eea45820a33e7b57072e49c37f0fbf40e 0xfc03f894465e2b43be15a56918c4e298e2ee4be5 0xe2709b901d6ea39ffca044679b4e268f65c68661 0x532915251c7dc45fca323a76e7726cb77b2316e6 0xd12c62dea4f5c705b38f4b034c3561ca65be71d5 0x6fbca37a3d4933f1ec9419a4c3da5d5329cddfc2 0x6a643bcc171e12448aa4202db2bfd4b008108a5a 0xe21b36ebede73eb8acc7e15e13407d629240cfbf 0x68db90264b5f95032110965e2b4ca7353d67f9f5
0xf3b5f18add21b6578e679d0de8ac7597d0095b73 0xbb3a0ceeea78fc630ea6ac4c97eecd106aefa16e 0xfd0041184f9387a822216be34da1f4893ea7b426 0x227fbcb2931d501a31f29b1a356e12f71c6deb8d 0x9aa1575e60d33cd8e750f3193bdfa7d5540fe136 0x76fc58dd26ed16baf40a893faef7920afd679036 0x0b61e8ce1efc73078db28b8dc9ae6e635efe67dd 0xa050e41f634170149c3b151729260df037a0f946
0xfb0cebff8dc1bd2b5538a6cea756477a3cbc3e4c 0xf45be6d4b50431cb7787075ec5b1b9b957aa19ba 0xe44717f479e36b428d105f9594c1e1e33c3003cb 0x2a89216e0135be6cae98fb207cb024b96de980c3 0x0941f8f756e890b2d81f7f16970a872ce0ae4001 0xc6cbb0774096f5309dcea918b30b32e194cbebc1 0xac0ad531c8570d87eb30e47fc9307f48304fa0d7 0xdb520b6769df9df5911e5969d570ea12850dac69 0xe0735dc521947f398d26184df05ca3803474eefd 0xa0aa179edad782f0dd3e71847379e3a3707041ff 0x897aaceb5620805a04b561c076ca49667d663238
0xa69bde39bafa75534befd12a5f36ec8f95248009 0x5c411a8ffc9965d7364d8edf29ab4a14aae3cb31 0x1d639c172c474d56ef85dae0431295466734c197
```


![image](https://github.com/onizukais/sybil-check/assets/170208261/63f260d3-ba30-45df-b1de-b981655352b9)

The addresses have the same on-chain activity. Their L0 interaction are the exact same, the same DAPPS in the same order in the same timespan. For example, their latest L0 interaction all are the same, and follow the exact same pattern : Stargate 4 months ago, Stargate 6 months ago and Merkly 8 months ago. This is the result of a script.

<img width="353" alt="image" src="https://github.com/onizukais/sybil-check/assets/170208261/da68e259-c311-420c-9f51-6a6831531735">
<img width="368" alt="image" src="https://github.com/onizukais/sybil-check/assets/170208261/79f56597-6d02-4628-a986-65507576d9d8">
<img width="344" alt="image" src="https://github.com/onizukais/sybil-check/assets/170208261/795cd6fd-615e-48a3-80b8-7cad10ecd15a">
<img width="359" alt="image" src="https://github.com/onizukais/sybil-check/assets/170208261/23366008-04ad-4d27-927b-0768f6297c9f">


These addresses share the same CEX deposit address, are part of a cluster with multiple internal links, and exhibit the same on-chain behavior. This suggests a large-scale sybil operation, likely automated by scripts. 


CLUSTER134

The first 20 addresses of the cluster share the same Binance deposit address: 0x6D60a11DD352Fdb2Fb675132D12fBEf0bF89512F. The remaining addresses are linked to numerous other addresses within the cluster multiple times.

```
0xb41a34389ec99fcca5a9a60b9c7df96480f189ba 0x2820766519271fa0b056c060229dbc1e003c11a4
0xb6825b1d069824678db46477d2a35d4b6445a66b
0xd9ae0f4453a78b56552c3027b703962b8c2f0c28 0x3b641ffbfb31a36197a3b325bd6f7f37a78c0f8b 0x7cef36004c7d0e4c3b2498badbc6b750124f0e9a 0xbaa6fc53c0dbb7b39b02686e997ef7270ea420a1 0xb8281a7caf09bb7a74c6db3c188f1aa4d528ab6f 0x835e80f167dd6ae0713591b667abb35ce0150dbf 0xabe7a565b02798afc330ec3ac5b04cfea55e30b3 0x05ccc4031ca946a46c19f644790575598ec900c1
0x17c436f245184d902893ec20d4df99c7cc97e289 0x3d7c8871fb724387a307cb80a5c2926353e9fa7e 0xdad138edaff8ad93983583da55cf24af7847aa8c 0x4a179a9e4de209181458167825b2a6d7218a226c
0xc5c7753124844f93c3b82dbbdf3be62c2261e847 0xe5729387f45ad13ac4557fbdf678ed9173e0e58d 0xfad4191108fd3eb32281555ed3bfc2b7ecc1144c 0xb8ba190f7efba2cd3dda281240482b8c4b722998 0x813acf9cb6198dd0fd5de4e5570d5b712253db41
```


![image](https://github.com/onizukais/sybil-check/assets/170208261/74015939-b8b7-404a-b262-c9b67204c53c)

The addresses have the same on-chain activity. Their L0 interaction are the exact same, the same DAPPS in the same order in the same timespan. For example, their latest L0 interaction all are the same, and follow the exact same pattern : WOOFi 1 month ago, Stargate 3 months ago and WOOFi 7 months ago. This is the result of a script.


<img width="295" alt="image" src="https://github.com/onizukais/sybil-check/assets/170208261/ac85d09c-50c4-4ced-86b7-87ac8dad3319">
<img width="339" alt="image" src="https://github.com/onizukais/sybil-check/assets/170208261/3d0d504c-24cf-4d9b-8f4c-bd1f36740ea0">
<img width="323" alt="image" src="https://github.com/onizukais/sybil-check/assets/170208261/1ff72bcc-8db0-4c8d-b2ee-55e5ce39b567">
<img width="322" alt="image" src="https://github.com/onizukais/sybil-check/assets/170208261/5d6cc34e-aeaa-4fab-a147-0d7f45ec6eb1">
<img width="375" alt="image" src="https://github.com/onizukais/sybil-check/assets/170208261/7efa95a6-eebf-4d7d-8c3e-1281c398d7a1">

These addresses share the same CEX deposit address, are part of a cluster with multiple internal links, and exhibit the same on-chain behavior. This suggests a large-scale sybil operation, likely automated by scripts. 


CLUSTER140


The first 11 addresses of the cluster share the same Binance deposit address: 0x77AfB814E97e3Cf45308ee314f8D2921cD7083bf. The remaining addresses are linked to numerous other addresses within the cluster multiple times.

```
0x6ebebeedac0e22a4e958d6673db8966a66ed55f1 0xda9f35777a672c8036acebf9a571f979df0f85e1 0x78e1c70ec76404f6ebc48eaf8392a9192023dfa9 0x074a90e19ab552ff39bcad27b2860e06f01f1db8 0xaff33f84688c789c455994e76892466ae0de9f28 0x7bb3d0637242b7b3f771a690d51abccb0a8b596a 0xa98737dceba65dae7264bd77fdef41244f53be07 0xe325f4a40ab8434b4584be3f795fa32d1420af60 0xf195659048de4e1025144bd8448058e97bfe705e
0x491ca7088ff9f33cf0bed47838053a19c556c509 0x44851030ac919488795b55d4e49be007a5b9e76a
0xd5071389ac374e5ce1047b9385de4e94f63b9dcc 0x02a58dfaad09b2fc5652a84d49266d49294ae414 0xea660d6a51faf05219c3479194376a1572249aff 0xf4230c95e6930a51e35c4ef778ff62f4d02e04b0 0x08a6f499052a84ba394a2bd50d312afa9f266676 0x91730c0fd232f1fede82ce3c0f520273246278cd 0xf1cbd1dfded153ef69881102d3e550ed231d257f 0x2202e14d55a9ead454755e717f8f1ec62fc529fd 0xc0c3b86f9499ecf851f9343d9948337d831e13af 0x77f4080a3b55c91a1dcfd37a3b2ff46ca166ff37 0xa454c2ba627bfcda86376d32421e00435453f39b 0xcb621b3e1a68806c68360998192514d48b7deddf 0xcdfc96bcd4375eb47963e20446c50277de9873f4 0x179fbc12c5f5347a2add79ca25f86a9a34d03abb 0x55cf872a76e35114bc56d48282f6157f266a36df 0xf555379f7e7545c95c1679219396e5dda01038d0
0x9890686a25e6f6e659cebc43bad5fcd6e8d89665 0xae4fd425c5ea5e9730c8756643eefe1e60026882 0x9de757c4058a07e39857452dc1950218b0e7c89d
0xa08b0febac3e7f34af697bd30fccc4f2dacdfb43
```

![image](https://github.com/onizukais/sybil-check/assets/170208261/1a80a813-36c4-479c-ae67-afb5cd883ad1)


The addresses have the same on-chain activity. Their L0 interaction are the exact same, the same DAPPS in the same order in the same timespan. For example, their latest L0 interaction all are the same, and follow the exact same pattern : Stargate 8 months ago, Stargate 9 months ago and Stargate 10 months ago. This is the result of a script.

<img width="327" alt="image" src="https://github.com/onizukais/sybil-check/assets/170208261/99429fe9-49f9-49f2-bfc0-a07a487d9803">
<img width="340" alt="image" src="https://github.com/onizukais/sybil-check/assets/170208261/22cd4d74-3c88-426f-a312-66000a883c37">
<img width="322" alt="image" src="https://github.com/onizukais/sybil-check/assets/170208261/60d43293-b107-402a-93fa-ab5e54c8dd35">
<img width="361" alt="image" src="https://github.com/onizukais/sybil-check/assets/170208261/2ca8731a-3d65-4fad-91b2-8993f76d25bb">
<img width="352" alt="image" src="https://github.com/onizukais/sybil-check/assets/170208261/85b40371-f7ce-4496-a018-ce4828d5c883">

These addresses share the same CEX deposit address, are part of a cluster with multiple internal links, and exhibit the same on-chain behavior. This suggests a large-scale sybil operation, likely automated by scripts.


CLUSTER141

The first 9 addresses of the cluster share the same OKX deposit address: 0x7Ba97387368D5A22baEbb4ccBeeE9Dca3D66BBF0. The remaining addresses are linked to numerous other addresses within the cluster multiple times.

```
0x8d52d8e2791ce7b942de48be7b35628b8c249d65 0xbd3b9ef63c79d0dc206aeb1feba35e68c7dd16b9 0xe9ff81d9c90a15e40a53e458a36bc701c9f80592 0x5015646e9be3bf88e0ddff05c3d494ae5da589fa 0xca33c9351674ae7db448fb15626782e53bf21a93 0x2239978c3e75ec0784f7f69356bd8235d0a7cbe5 0x95815b4d8a53b02b37f9c21b8dddad349a87669f 0x973e848eec772e3f7bb3d36091775b275b23ac25 0x06abef993c9674b6c69f87316e36d58d67d32d31 0x78c413fb2745f07ead4b0c20bcf7f2945ed94515 0x1e06c650bba984039f6e2a55b7f8fc816cc9920b 0x193f24bb16d4051938f3586bcae7532a7dcb0e25 0xd91e3059b2201574060d2877079aec9cfeeee0e4 0x8daf4f49749601f20978c4821bfa5e4038a6bd57 0x3fc0672d46ccaf0f8d485500ec049de17d7bf876 0xbaca7fb21dc628212f556f9e473b80aadac91b8e 0x148cf92066f1d9502914ff001c3aaf828db61238 0xd336713a56624b67d562376eba38105d27d8eff3 0xaa6293a662f7797b8a52335b1bee15a308d89da0 0xdf7b565ba908584a8967fc9aa43c79662bf0a213 0x5975d8155b3f0c0e9d2167a2fa362d2fbcc889df 0xc4775d714038ad50692bb29b95e44243bcc0f411 0xf0dfc87d290ef093354b9203f9493c70d17ea784 0xb73ff0c92b9e91a832482b5271b79afc649cc68e
```
<img width="275" alt="image" src="https://github.com/onizukais/sybil-check/assets/170208261/161b5214-d0c2-4f6c-9a98-1b9acd78059d">


The addresses have the same on-chain activity. Their L0 interaction are the exact same, the same DAPPS in the same order in the same timespan. For example, their latest L0 interaction all are the same, and follow the exact same pattern : Stargate 2 months ago, Omni X 4 months ago, Omni X 6 months ago and Stargate 7 months ago. This is the result of a script

<img width="295" alt="image" src="https://github.com/onizukais/sybil-check/assets/170208261/602c1df6-5872-476f-baf2-4f9d59e4c73b">
<img width="306" alt="image" src="https://github.com/onizukais/sybil-check/assets/170208261/ae85926a-199d-447d-8ba0-26e7bce3bfb9">
<img width="306" alt="image" src="https://github.com/onizukais/sybil-check/assets/170208261/1be85576-f7ff-4416-9181-a42c23fcbd60">
<img width="323" alt="image" src="https://github.com/onizukais/sybil-check/assets/170208261/cf15a86d-573c-4183-bf1f-e57ff8ab3b07">



These addresses share the same CEX deposit address, are part of a cluster with multiple internal links, and exhibit the same on-chain behavior. This suggests a large-scale sybil operation, likely automated by scripts. 


CLUSTER143

The first 10 addresses of the cluster share the same OKX deposit address: 0x805656a6c89AC7a0e8097914EDCD9c0330c94513. The remaining addresses are linked to numerous other addresses within the cluster multiple times.

```
0x5e611e445b62ee4ece67b58996d64ab9942cbad3 0xa183153598dba79f7eea16dca12ab302d7d13dff 0x929e2d8f92eda8e5cf6f841ec3a1088497154c50 0xbdd28ed88764c8a0fc25fbe11630ff073f3ae851 0x35a901098cf337b41a13bc0f245547497b384871
0xa22f00f8afd919dcc53b0ee70a6c4ba118006a46 0x8c9bf54b263ddc5c0fc9f7f84d51ecc4e67a56d6 0x90795c9eed0c18f031c3329143aa089eadfb70ea 0xd7018846e545e48ae44876b55a40c7c2667e7a0b 0x5a8403c52889994192b1a7500b40ba03d05be6b0
0xb62287c0779c25ec259c1efcb5c46940f22113b9 0xad73ad629f2664d72d481d55264f496fb30bb20c 0x57e16f8e90fb0ce7edb8caa30850ee0ffeab27ac 0x16069678277bac3739eb3c3199c89dd4e77627a1
0xcf4a907e647f5472d3a8a5021d0a7e4f04d7b00c 0x0a3e520aa26736e9ccba6495b2205c585e8d01a0 0xde5cef34e94f1f255d686b6eb45cde8726f15b2e 0x7a2ca1232086539bb82472146f6200da5110e5c4
0x7ac7ee6da0ff7c21643755d1dd9451e54b21d6d6 0x823b61a564d28e76896ac6b3c5e9b0ca8706fcdf 0xa08fd3d3949bc63534f7ec887c80595e845c167e 0x52b519edf17310fb0ca7e9d82a2762b3f6b5a4a4
```

![image](https://github.com/onizukais/sybil-check/assets/170208261/33a1e59f-5b74-4475-808d-2562ccc5141d)


The addresses have the same on-chain activity. Their L0 interaction are the exact same, the same DAPPS in the same order in the same timespan. For example, their latest L0 interaction all are the same, and follow the exact same pattern : Stargate 1 month ago, Stargate 6 months ago, Testnet 11 months ago and Stargate 1 year ago. This is the result of a script.


<img width="316" alt="image" src="https://github.com/onizukais/sybil-check/assets/170208261/8e7b65b2-a201-443e-8f3c-e325e732085a">
<img width="305" alt="image" src="https://github.com/onizukais/sybil-check/assets/170208261/b519d83b-5358-45ea-85c6-25d277527690">
<img width="323" alt="image" src="https://github.com/onizukais/sybil-check/assets/170208261/a0d1dfd3-4d02-474b-8e21-219d5219a499">
<img width="323" alt="image" src="https://github.com/onizukais/sybil-check/assets/170208261/1c1b5728-2f84-4dd6-b857-b738b4cac2a1">
<img width="323" alt="image" src="https://github.com/onizukais/sybil-check/assets/170208261/a7f98660-7f2e-481e-845d-644f359960a9">
<img width="323" alt="image" src="https://github.com/onizukais/sybil-check/assets/170208261/ffc06019-5355-49ae-95b8-d4ce9dd9c0da">
<img width="305" alt="image" src="https://github.com/onizukais/sybil-check/assets/170208261/8e01af36-c9da-4e92-a8eb-e7a7783e0dd5">

These addresses share the same CEX deposit address, are part of a cluster with multiple internal links, and exhibit the same on-chain behavior. This suggests a large-scale sybil operation, likely automated by scripts.


CLUSTER147

The first 8 addresses of the cluster share the same Binance deposit address: 0x89F45Cbb309850aa14eCd27fA9EDD735Aea723bB. The remaining addresses are linked to numerous other addresses within the cluster multiple times.

```
0xeccbb285157b89425a420175deebc22b2f4acac5 0x26e61d34607a6b6181126b9964d30f0f79743a5a
0x777f747095d28606a5d7f6518aee98f8061c221f
0xc35433503f08a011f12bc29b3e38e8a473b8a490 0x13be4da539271084a17059e3faa80e12d254fc19 0x8cdb82c657a4f0cdf643760950d0344478c356b5 0x9004a397dcad504cccb4c1e8aeaf0307467cdca1 0x59975f0f2ac0f8999a991075d625f907abce928b 0x5abfb9a3575767e802a62e3af4cc1179f0e5dfc7 0xdfb2eb4436f8ec9d0a4524f4c4479a23c92dccff 0xa29de1ce221afc3e51407d5db907f7f68baa7437 0xe61f43464b3f46b4cd8841cf77755c540f128151
0x15e30badf9027a81ab182c1e59045ceb63ed4d3d 0xb16ff090dee668e23e206e51cc5ef5390cbb6ffb 0x77161be5596f8614ad336472c3c8460576da4625
0x4c65e047c7fc28cbdfb8e9ca15fb10f0666eae2b 0x16148617384f70e0db33449fe15459e7ca7877bc
0x9f3c9ad03cd27923bef7a58ea1d1a7517094111f 0x1b908a0d71302fc576e1fb08684ece1710befab2 0xb4262e8788c9c8f1453605f217857673a719337a
0x582c6f6f915070c3ea2238d073740c8f4a1c35d1 0x59a24315f63d1668c5ddb2f9ba01f69c35d2bfbe 0x604933190cd5f32a12657a4fecfc2367ce119ce0 0xecd767a9e18151cb9de8967ca64899a42a5636f1 0x7edd0d25acadae9c57588afd6ed9da7c0e6f9809 0x44c94de425ab22d2834302d857a90039ec334a80
0x5c97d7d8052934757517f09aabe26fd582598228
0x09aa3fd1996a81973e86463f63c175103e8c840e
```

![image](https://github.com/onizukais/sybil-check/assets/170208261/5dfbb310-4221-4f7e-b171-5c2c8051c080)


The addresses have the same on-chain activity. Their L0 interaction are the exact same, the same DAPPS in the same order in the same timespan. For example, their latest L0 interaction all are the same, and follow the exact same pattern : Merkly 4 months ago, Merkly 6 months ago, Merkly 9 months ago and Merkly 10 months ago. This is the result of a script.



<img width="331" alt="image" src="https://github.com/onizukais/sybil-check/assets/170208261/f85d845e-805b-4eb2-9690-5a739033ef83">
<img width="338" alt="image" src="https://github.com/onizukais/sybil-check/assets/170208261/d3cb0094-7323-4004-afae-e1f10aac2dc2">
<img width="337" alt="image" src="https://github.com/onizukais/sybil-check/assets/170208261/a38d0010-dc21-4d2b-b14d-680930046570">

These addresses share the same CEX deposit address, are part of a cluster with multiple internal links, and exhibit the same on-chain behavior. This suggests a large-scale sybil operation, likely automated by scripts.







CLUSTER8

8,0x838f634Ce176DC5B6B36853db87A671A222C59FE



0x0b61e8ce1efc73078db28b8dc9ae6e635efe67dd
0xe895909b9cc3000ae3e6008ede594b9f7f0f870b
0x2a89216e0135be6cae98fb207cb024b96de980c3
0x49c0f7df4c6d2edbe88b1e52150d2c2f02a77458
0xdb520b6769df9df5911e5969d570ea12850dac69
0x76fc58dd26ed16baf40a893faef7920afd679036
//
0x50270d3eea45820a33e7b57072e49c37f0fbf40e
0x2d232c211c80c8ce716b884b8fcd784bb55e6053
0xe2709b901d6ea39ffca044679b4e268f65c68661
//
0xfb0cebff8dc1bd2b5538a6cea756477a3cbc3e4c
0x8d8979ba8c18e0591f08cdefa54980a13b71df1b
0x1d639c172c474d56ef85dae0431295466734c197
0x0941f8f756e890b2d81f7f16970a872ce0ae4001
0x6fbca37a3d4933f1ec9419a4c3da5d5329cddfc2
0x4f2dc64360ebbe78c968338ed4baae1d14144340
0x2caaa9c911de5990b474eb5c7679b8662d931eb2
0xa69bde39bafa75534befd12a5f36ec8f95248009
0xf59a93cf770eb6e2b4344387ce835c58ff8b363d
0xe44717f479e36b428d105f9594c1e1e33c3003cb
0xe0735dc521947f398d26184df05ca3803474eefd
0x227fbcb2931d501a31f29b1a356e12f71c6deb8d
0x68db90264b5f95032110965e2b4ca7353d67f9f5
0xf3f4ee03357483b3b41a1d58b32dc1f57bd29c10
0x6a643bcc171e12448aa4202db2bfd4b008108a5a
0x8cb50b46e0708dc0b2b34e6077b876eb95a057af
0xb339297171670de477002e1e3bd429b87d2da263
0xad8a954fab2e71f3865a8272c4042e10d83e3d5f
0x9aa1575e60d33cd8e750f3193bdfa7d5540fe136
0xe21b36ebede73eb8acc7e15e13407d629240cfbf
0xa0aa179edad782f0dd3e71847379e3a3707041ff
0xfd0041184f9387a822216be34da1f4893ea7b426


(0x838f634Ce176DC5B6B36853db87A671A222C59FE, 0x0b61e8ce1efc73078db28b8dc9ae6e635efe67dd, 0xe895909b9cc3000ae3e6008ede594b9f7f0f870b, 0x2a89216e0135be6cae98fb207cb024b96de980c3, 0x49c0f7df4c6d2edbe88b1e52150d2c2f02a77458, 0xdb520b6769df9df5911e5969d570ea12850dac69, 0x76fc58dd26ed16baf40a893faef7920afd679036, 0x50270d3eea45820a33e7b57072e49c37f0fbf40e, 0x2d232c211c80c8ce716b884b8fcd784bb55e6053, 0xe2709b901d6ea39ffca044679b4e268f65c68661, 0xfb0cebff8dc1bd2b5538a6cea756477a3cbc3e4c, 0x8d8979ba8c18e0591f08cdefa54980a13b71df1b, 0x1d639c172c474d56ef85dae0431295466734c197, 0x0941f8f756e890b2d81f7f16970a872ce0ae4001, 0x6fbca37a3d4933f1ec9419a4c3da5d5329cddfc2, 0x4f2dc64360ebbe78c968338ed4baae1d14144340, 0x2caaa9c911de5990b474eb5c7679b8662d931eb2, 0xa69bde39bafa75534befd12a5f36ec8f95248009, 0xf59a93cf770eb6e2b4344387ce835c58ff8b363d, 0xe44717f479e36b428d105f9594c1e1e33c3003cb, 0xe0735dc521947f398d26184df05ca3803474eefd, 0x227fbcb2931d501a31f29b1a356e12f71c6deb8d, 0x68db90264b5f95032110965e2b4ca7353d67f9f5, 0xf3f4ee03357483b3b41a1d58b32dc1f57bd29c10, 0x6a643bcc171e12448aa4202db2bfd4b008108a5a, 0x8cb50b46e0708dc0b2b34e6077b876eb95a057af, 0xb339297171670de477002e1e3bd429b87d2da263, 0xad8a954fab2e71f3865a8272c4042e10d83e3d5f, 0x9aa1575e60d33cd8e750f3193bdfa7d5540fe136, 0xe21b36ebede73eb8acc7e15e13407d629240cfbf, 0xa0aa179edad782f0dd3e71847379e3a3707041ff, 0xfd0041184f9387a822216be34da1f4893ea7b426)

https://platform.arkhamintelligence.com/visualizer/entity/0x838f634Ce176DC5B6B36853db87A671A222C59FE,0x0b61e8ce1efc73078db28b8dc9ae6e635efe67dd,0xe895909b9cc3000ae3e6008ede594b9f7f0f870b,0x2a89216e0135be6cae98fb207cb024b96de980c3,0x49c0f7df4c6d2edbe88b1e52150d2c2f02a77458,0xdb520b6769df9df5911e5969d570ea12850dac69,0x76fc58dd26ed16baf40a893faef7920afd679036,0x50270d3eea45820a33e7b57072e49c37f0fbf40e,0x2d232c211c80c8ce716b884b8fcd784bb55e6053,0xe2709b901d6ea39ffca044679b4e268f65c68661,0xfb0cebff8dc1bd2b5538a6cea756477a3cbc3e4c,0x8d8979ba8c18e0591f08cdefa54980a13b71df1b,0x1d639c172c474d56ef85dae0431295466734c197,0x0941f8f756e890b2d81f7f16970a872ce0ae4001,0x6fbca37a3d4933f1ec9419a4c3da5d5329cddfc2,0x4f2dc64360ebbe78c968338ed4baae1d14144340,0x2caaa9c911de5990b474eb5c7679b8662d931eb2,0xa69bde39bafa75534befd12a5f36ec8f95248009,0xf59a93cf770eb6e2b4344387ce835c58ff8b363d,0xe44717f479e36b428d105f9594c1e1e33c3003cb,0xe0735dc521947f398d26184df05ca3803474eefd,0x227fbcb2931d501a31f29b1a356e12f71c6deb8d,0x68db90264b5f95032110965e2b4ca7353d67f9f5,0xf3f4ee03357483b3b41a1d58b32dc1f57bd29c10,0x6a643bcc171e12448aa4202db2bfd4b008108a5a,0x8cb50b46e0708dc0b2b34e6077b876eb95a057af,0xb339297171670de477002e1e3bd429b87d2da263,0xad8a954fab2e71f3865a8272c4042e10d83e3d5f,0x9aa1575e60d33cd8e750f3193bdfa7d5540fe136,0xe21b36ebede73eb8acc7e15e13407d629240cfbf,0xa0aa179edad782f0dd3e71847379e3a3707041ff,0xfd0041184f9387a822216be34da1f4893ea7b426?flow=self&positions=%7B%7D&sortDir=desc&sortKey=time&usdGte=0.1

https://platform.arkhamintelligence.com/visualizer/entity/0x838f634Ce176DC5B6B36853db87A671A222C59FE,0x50270d3eea45820a33e7b57072e49c37f0fbf40e,0x2d232c211c80c8ce716b884b8fcd784bb55e6053,0xe2709b901d6ea39ffca044679b4e268f65c68661,0xfb0cebff8dc1bd2b5538a6cea756477a3cbc3e4c,0x8d8979ba8c18e0591f08cdefa54980a13b71df1b,0x1d639c172c474d56ef85dae0431295466734c197,0x0941f8f756e890b2d81f7f16970a872ce0ae4001,0x6fbca37a3d4933f1ec9419a4c3da5d5329cddfc2,0x4f2dc64360ebbe78c968338ed4baae1d14144340,0x2caaa9c911de5990b474eb5c7679b8662d931eb2,0xa69bde39bafa75534befd12a5f36ec8f95248009,0xf59a93cf770eb6e2b4344387ce835c58ff8b363d,0xe44717f479e36b428d105f9594c1e1e33c3003cb,0xe0735dc521947f398d26184df05ca3803474eefd,0x227fbcb2931d501a31f29b1a356e12f71c6deb8d,0x68db90264b5f95032110965e2b4ca7353d67f9f5,0xf3f4ee03357483b3b41a1d58b32dc1f57bd29c10,0x6a643bcc171e12448aa4202db2bfd4b008108a5a,0x8cb50b46e0708dc0b2b34e6077b876eb95a057af,0xb339297171670de477002e1e3bd429b87d2da263,0xad8a954fab2e71f3865a8272c4042e10d83e3d5f,0x9aa1575e60d33cd8e750f3193bdfa7d5540fe136,0xe21b36ebede73eb8acc7e15e13407d629240cfbf,0xa0aa179edad782f0dd3e71847379e3a3707041ff,0xfd0041184f9387a822216be34da1f4893ea7b426?flow=self&positions={}&sortDir=desc&sortKey=time&to=0x838f634Ce176DC5B6B36853db87A671A222C59FE&usdGte=0.1

CLUSTER26

8,0xBCbECC8543E341343C7f5399dd7ee3aE2E169c71



0x14b35ea598a18e171a8f1e724c356f83fb4a0f18
0xfcc49e880b3a024d2a31742178d86ca5cfe0169d
0x541bc299778baa8157a5bb093099791ff05b0cc4
0x7b6ac5df584f466fa8670b1107638dc7e940796f
0xd324c3e1da374f29077ca33d2e669456f897d80e
0x00a104b51215180cd87071962567cdff6961e0b7
0xe5174798675530e1ccac4d121aa56d67c8b0bd3c
0x98db5698bd3bbc83812d2a8e03e1411b847310ac
//
0x105d326450701879833e3cd33f161493f082902d
0x76cd684cb4b6148f667e6ee7896e2f6fcb3caa7e
0x682463b16fcb871a17d4fb70a504fca7e4414b83
0xb4d77e9a11425f8bb6924b374385282bf35a97d5
0x4040ae6e1d67cc47060871ed9dd7c3eee7ad5284
0xc729d5a6eb0caaf27f4a68f31545ee88c252a0a1
//
0x558fbb1b9dde11c85da59dee9b399bf37016a999
0x73f13a414d820b5e9118713c7466985890d2bbe8
0x106829fc39b9e826f694686b0211d54c710e3dea
0xc8a60f7fc1ca1e2c1c13ee85ee1130024f69b07f
0x692a15eab43e79f511abd4c26713c32301ec0252
0xb1a9c3c1841e55be6486d7844c2f8c791ea0d6d9


(0xBCbECC8543E341343C7f5399dd7ee3aE2E169c71, 0x14b35ea598a18e171a8f1e724c356f83fb4a0f18, 0xfcc49e880b3a024d2a31742178d86ca5cfe0169d, 0x541bc299778baa8157a5bb093099791ff05b0cc4, 0x7b6ac5df584f466fa8670b1107638dc7e940796f, 0xd324c3e1da374f29077ca33d2e669456f897d80e, 0x00a104b51215180cd87071962567cdff6961e0b7, 0xe5174798675530e1ccac4d121aa56d67c8b0bd3c, 0x98db5698bd3bbc83812d2a8e03e1411b847310ac, 0x105d326450701879833e3cd33f161493f082902d, 0x76cd684cb4b6148f667e6ee7896e2f6fcb3caa7e, 0x682463b16fcb871a17d4fb70a504fca7e4414b83, 0xb4d77e9a11425f8bb6924b374385282bf35a97d5, 0x4040ae6e1d67cc47060871ed9dd7c3eee7ad5284, 0xc729d5a6eb0caaf27f4a68f31545ee88c252a0a1, 0x558fbb1b9dde11c85da59dee9b399bf37016a999, 0x73f13a414d820b5e9118713c7466985890d2bbe8, 0x106829fc39b9e826f694686b0211d54c710e3dea, 0xc8a60f7fc1ca1e2c1c13ee85ee1130024f69b07f, 0x692a15eab43e79f511abd4c26713c32301ec0252, 0xb1a9c3c1841e55be6486d7844c2f8c791ea0d6d9)

https://platform.arkhamintelligence.com/visualizer/entity/0xBCbECC8543E341343C7f5399dd7ee3aE2E169c71,0x14b35ea598a18e171a8f1e724c356f83fb4a0f18,0xfcc49e880b3a024d2a31742178d86ca5cfe0169d,0x541bc299778baa8157a5bb093099791ff05b0cc4,0x7b6ac5df584f466fa8670b1107638dc7e940796f,0xd324c3e1da374f29077ca33d2e669456f897d80e,0x00a104b51215180cd87071962567cdff6961e0b7,0xe5174798675530e1ccac4d121aa56d67c8b0bd3c,0x98db5698bd3bbc83812d2a8e03e1411b847310ac,0x105d326450701879833e3cd33f161493f082902d,0x76cd684cb4b6148f667e6ee7896e2f6fcb3caa7e,0x682463b16fcb871a17d4fb70a504fca7e4414b83,0xb4d77e9a11425f8bb6924b374385282bf35a97d5,0x4040ae6e1d67cc47060871ed9dd7c3eee7ad5284,0xc729d5a6eb0caaf27f4a68f31545ee88c252a0a1,0x558fbb1b9dde11c85da59dee9b399bf37016a999,0x73f13a414d820b5e9118713c7466985890d2bbe8,0x106829fc39b9e826f694686b0211d54c710e3dea,0xc8a60f7fc1ca1e2c1c13ee85ee1130024f69b07f,0x692a15eab43e79f511abd4c26713c32301ec0252,0xb1a9c3c1841e55be6486d7844c2f8c791ea0d6d9?flow=self&positions=%7B%7D&sortDir=desc&sortKey=time&usdGte=0.1

https://platform.arkhamintelligence.com/visualizer/entity/0xBCbECC8543E341343C7f5399dd7ee3aE2E169c71,0x105d326450701879833e3cd33f161493f082902d,0x76cd684cb4b6148f667e6ee7896e2f6fcb3caa7e,0x682463b16fcb871a17d4fb70a504fca7e4414b83,0xb4d77e9a11425f8bb6924b374385282bf35a97d5,0x4040ae6e1d67cc47060871ed9dd7c3eee7ad5284,0xc729d5a6eb0caaf27f4a68f31545ee88c252a0a1,0x558fbb1b9dde11c85da59dee9b399bf37016a999,0x73f13a414d820b5e9118713c7466985890d2bbe8,0x106829fc39b9e826f694686b0211d54c710e3dea,0xc8a60f7fc1ca1e2c1c13ee85ee1130024f69b07f,0x692a15eab43e79f511abd4c26713c32301ec0252,0xb1a9c3c1841e55be6486d7844c2f8c791ea0d6d9?flow=self&positions={}&sortDir=desc&sortKey=time&to=0xBCbECC8543E341343C7f5399dd7ee3aE2E169c71&usdGte=0.1








 
