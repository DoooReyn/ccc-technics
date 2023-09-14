```typescript
changeCloth (skinName: string, slotName: string): any {
    let spine: sp.Skeleton = this.node.spine
    let skeletonData = spine.skeletonData.getRuntimeData()
    let skin = skeletonData.findSkin(skinName)
    const slot = spine.findSlot(slotName)
    const slotIndex = skeletonData.findSlotIndex(slotName)
    const attachment = skin.getAttachment(slotIndex, slotName)
    slot.setAttachment(attachment)
  }
```

另外可以参考：[web/原生多平台 Spine 换装方案 by 羽毛先生](https://mp.weixin.qq.com/s?__biz=MjM5ODAxNTM2NA==&mid=2659689343&idx=1&sn=f51cb29996444a81b660bce76c985551&chksm=bda23b948ad5b282bb220f94afa92491aa21ee672c48e4de19ee0664b6e1b7c0f9c187c5a7a3&scene=21#wechat_redirect)