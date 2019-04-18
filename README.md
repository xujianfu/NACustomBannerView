# NACustomBannerView
封装轮播图、更改UIPageControl的样式

使用方法
let x = (SCREEN_WIDTH - 335)/2
let frame = CGRect(x: x, y: CGFloat(21), width: 335, height: 170)
let urls = ["http://p.lrlz.com/data/upload/mobile/special/s252/s252_05471521705899113.png",              "http://p.lrlz.com/data/upload/mobile/special/s303/s303_05442007678060723.png",                  "http://p.lrlz.com/data/upload/mobile/special/s303/s303_05442007587372591.png",                    "http://p.lrlz.com/data/upload/mobile/special/s303/s303_05442007388249407.png",                    "http://p.lrlz.com/data/upload/mobile/special/s303/s303_05442007470310935.png"]
cycleScrollView = NACustomBannerView(frame: frame, imageUrls: urls) { (index) in
   print("当前第\(index)张")
}
cycleScrollView.layer.masksToBounds = true
cycleScrollView.layer.cornerRadius = 5.0
container.addSubview(cycleScrollView)

