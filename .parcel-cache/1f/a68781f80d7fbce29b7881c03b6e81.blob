window.dom = {
    find(selector, scope){
        return (scope || document).querySelectorAll(selector)
    },
    style(node, name, value){
        if(arguments.length === 3){
            //dom.style(div, 'color', 'red')
            node.style[name] = value
        }else if (arguments.length === 2){
            if(typeof name === 'string'){
                // dom.style(div, 'color')
                return node.style[name]
            }else if(name instanceof Object){
                // dom.style(div,{color: 'red'})
                for(let key in name){
                    // key: border / color
                    // node.style.border = ...
                    // node.style.color = ...
                    node.style[key] = name[key]
                }
            }   
        }        
    },
    each(nodeList, fn){
        for(let i=0; i<nodeList.length; i++){
            fn.call(null, nodeList[i])
        }
    },
    
}