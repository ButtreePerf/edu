---
title: Roadmap
---

# 🛣️แนวทางเรียนรู้

ฟามรู้ตั้งแต่ศูนย์ไปจนถึงเดฟตัวเต็มวัย จะต้องรู้เรื่องอะไรบ้างหว่า? แล้วตัวไหนควรเริ่มเรียนเมื่อไหร่? หรือต้องรู้เรื่องอะไรก่อนหลัง? ในบทความนี้ **ดช.แมวน้ำ** อยากขอเสนอภาพรวมทั้งหมด (ที่ป๋มคิดว่า) ควรจะต้องรู้ โดยเรียงลำดับความสำคัญก่อนหลังให้เรียบย้อยแย้ว เชิญเสพได้เรยฮั๊ฟ

![banner](/img/roadmap.jpg)

> ภาพจาก [Microsoft Copilot](https://th.bing.com/th/id/OIG2.E7.tLA2qmOffSVaS_RbW?pid=ImgGn)

---

<link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css" rel="stylesheet" />

:::warning
แนวทางที่ป๋มนำมาแนะนำนี้ จะเป็นสายเดฟฝั่ง <Gray>Backend</Gray> และ <Gray>Architecture design</Gray> ซึ่งอาจไม่ใช่ตัวที่เหมาะกับทุกๆคน เพราะมันขึ้นอยู่กับ หน้างานที่เพื่อนๆได้รับ ความชอบความสนใจที่แต่ละคนมี บลาๆ ดังนั้นขอให้ดูแค่เป็นแนวทางนะกั๊ฟ ส่วนสายนี้เหมาะกับคนที่ชอบคิด ชอบเกมแก้ปัญหา ความสวยงามจะไม่สามารถมองเห็นได้ด้วยตา แต่สามารถสัมผัสได้ด้วยใจ 💓 จากการที่จิ๊กซอในระบบ มันเดินไปตามที่ออกแบบ ความเพลินของสายนี้คือการอ่านเกมให้ขาด
:::

## 🛸โพยการอัพสกิล
เพื่อความง่ายในการเรียน **ดช.แมวน้ำ** จะขอคัดมาเฉพาะตัวที่เด็ดๆก่อน ไม่งั้นตาลายแน่นวล ส่วนรายละเอียดที่ขาดหายไป เดี๋ยวจะค่อยกลับมาเติมลงในเพจนี้เรื่อยๆฮั๊ฟ
> สำหรับวัยรุ่นใจฮ้อน สามารถดูภาพรวมได้จากลิงค์นี้เยย [`สมาคมโปรแกรมเมอร์ไทย 🎉`](https://roadmap.thaiprogrammer.org) ซึ่งเพื่อนๆสามารถเข้าไปช่วยแปลกันได้นะกั๊ฟจากตรงนี้ [Github](https://github.com/ThaiProgrammer/tpa-roadmap)

<details>
  <summary>(จิ้มอย่างแผ่วเบา) เพื่อดูความหมายของรูป</summary>
  <div>
    <div>
        ```mermaid
        flowchart
            Simple[เนื้อหาจบได้ด้วยตัวมันเอง]
            Complex[[มีรายละเอียดเยอะม๊วก\nแตกแขนงออกไปอีกหลายตัว]]
        ```
        ```mermaid
        flowchart
            A[A]-->AA[ต้องเรียน A ก่อน\nถึงจะเรียนก้อนนี้ได้]
            B[B]-.->BB["ไม่ต้องเรียน B ก็เรียนก้อนนี้ได้\n(ถ้าเรียนมาก่อนจะเข้าใจง่ายขึ้น)"]
        ```
        ```mermaid
        flowchart
            code[fa:fa-robot\nการเขียนโค้ด]
            database[fa:fa-database\nฐานข้อมูล]
            testing[fa:fa-bug-slash\nการทดสอบระบบ]
            utility[fa:fa-gauge-high\nตัวช่วย]
            design[fa:fa-puzzle-piece\nการออกแบบ]
            system[fa:fa-user-secret\nการดูแลระบบ]
            cloud[fa:fa-cloud-bolt\nคลาวด์]
        ```
    </div>
  </div>
</details>

```mermaid
flowchart
    procedural[fa:fa-robot\nProcedural\nProgramming]-->database
    procedural-.->VersionControls[fa:fa-gauge-high\nVersion\nControls]
    procedural-->algorithm[fa:fa-robot\nData Structure\nand Algorithm]
    procedural-->oop["fa:fa-robot\nObject-Oriented\nProgramming (OOP)"]
    algorithm-.->oop
    oop-->testing[[fa:fa-bug-slash\nTesting]]
    oop-->uml[fa:fa-gauge-high\nUML]
    oop-->design
    uml-.->design
    oop-->api[fa:fa-robot\nWeb API]
    api-->scaling
    scaling-->architecture
    api-.->design

    %% api-->security[Security]
    %% api-->docker[Docker]
    %% api-.->testing

    subgraph design[Designs & Principles]
        direction TB
        solid[fa:fa-puzzle-piece\nSOLID Designs]-.->design-patterns[fa:fa-puzzle-piece\nDesign Patterns]-->anti-patterns[fa:fa-puzzle-piece\nAnti-Patterns]

        %% ddd[fa:fa-puzzle-piece\nDomain Driven Design]
        %% tdd[fa:fa-puzzle-piece\nTest Driven Development]
        %% clean[fa:fa-puzzle-piece\nClean Architecture]
        %% cqrs[fa:fa-puzzle-piece\nCQRS]
    end


    subgraph database[Databases]
        direction TB
        relational-db[fa:fa-database\nRelational]
        relational-db-->NoSQL[[fa:fa-database\nNoSQL]]
    end

    subgraph scaling
        cloud[[fa:fa-cloud-bolt\nCloud\nComputing]]
        caching[[fa:fa-robot\nCaching]]
        monitoring[[fa:fa-user-secret\nSystem\nMonitoring]]
    end

    subgraph architecture[Architectures]
        direction TB
        monolith[fa:fa-puzzle-piece\nMonolith]-->microservices[fa:fa-puzzle-piece\nMicroservices]
        messaging[[fa:fa-puzzle-piece\nMessaging\n& Events]]

        %% Serverless
    end
```

## 😅ดูจบแล้วไงต่อ?
เนื้อหาทั้งหมดทุกตัวใน Roadmap จะถูกเรียงหมวดตามสัญลักษณ์ต่างๆ (<Icon icon="fa-solid fa-robot" /> <Icon icon="fa-solid fa-database" /> <Icon icon="fa-solid fa-bug-slash" /> <Icon icon="fa-solid fa-gauge-high" /> <Icon icon="fa-solid fa-puzzle-piece" /> <Icon icon="fa-solid fa-user-secret" /> <Icon icon="fa-solid fa-cloud-bolt" />) ซึ่งสามารถอ่านได้จากเว็บสลัดผักทั้งหมดเบย โดยกดที่เมนู [`🧑‍💻ฟามรู้`](/docs/category/contributions) ด้านบน หรือ จะแอบไปกดติดตามเพจสลัดผักไว้ก่อนก็ได้น้าา [`Facebook Mr.Saladpuk`](https://www.facebook.com/mr.saladpuk) ซึ่งในรอบนี้กระเป๋ม **ดช.แมวน้ำ** มีความตั้งใจที่จะค่อยๆทะยอยส่งมอบฟามรู้ให้กับเพื่อนๆอุ๊งๆของเรา และกำลังหาคนใจดีช่วยกันแชร์ความรู้ที่มีอยู่ในพุง โดยสามารถกดไปดูวิธีช่วยได้จากลิงค์นี่เบยกั๊ฟ [`🥳แบ่งปันฟามรู้`](/docs/contribute/creator)

:::note
เดี๋ยวถ้ามีเวลาจะกลับมาทำให้หน้านี้สามารถกดดูรายละเอียด และ พาเพื่อนๆไปยังบทความได้เลย รวมถึงระบบสมาชิกให้เพื่อนๆสามารถดูได้ว่ามีเนื้อหาไหนที่ยังไม่ได้ดู หรือ มีความรู้ตรงไหนอัพเดทใหม่ ให้จบเบ็ดเสร็จในหน้าเดียว แต่ตอนนี้ก็ยังไม่มีเวลาทำ ต้องขอโทษด้วยน้ากั๊ฟ 🙏
:::