
function setSliderWidth() {
    const p = document.getElementsByClassName('slider')[0];
    const c = document.getElementsByClassName('slider-group')[0];
    const ifLoop = true;
    let children = c.children;
    let width = 0;
　　//注意三个xxWidth值的区别，clientWidth包含了页面右侧滑轨的宽度
    // let sliderWidth = p.clientWidth;
    // let sliderWidth = p.offsetWidth;
    let sliderWidth = window.innerWidth;
    for(let i=0;i<children.length;i++) {
        let child = children[i];
        child.style.width = sliderWidth + 'px';
        width += sliderWidth;
    };
    if(ifLoop) {
        width += 2 * sliderWidth;
    };
    c.style.width = width + 'px';
}
