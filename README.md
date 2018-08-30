# wl-address
基于jq的自动化三级联动地址插件

引入wl-address.css 和 wl-address.css

// weilan三级地址联动插件 必须引入wl-address.js和./wl-address.css
    // 先实例化 并传入省市县地址请求api 目前默认传参数为pid 获取全部省份传空
    var wl = new WlAddress();
    wl.init({
      action: 'https://api.bai*****gchuang.com/App/****/area'
    });

    // 弹出地址选择
    function addrShow() {
      // 淡出地址请调用wl.show() 函数 当编辑时传入当前地址 如下注释部分 ，新增时无需传参
      wl.show({
        /* addr: {
          province: '河南省',
          provinceId: 410000,
          city: '郑州市',
          cityId: 410100,
          content: '金水区',
          contentId: 410105,
        } */
      });
    }

    // 获取选择后的地址数据
    function getAddr() {
      // 当地址选择完三级后会自动消失 请调用wl.getData()函数拿到你选择的地址数据
      var data = wl.getData();
      console.log(data)
    }
