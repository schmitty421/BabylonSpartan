

      //______________________________PREREQUISITES





        const canvas = document.getElementById('renderCanvas'); // Get the canvas element
        const engine = new BABYLON.Engine(canvas, true, { stencil: true }); // Generate the BABYLON 3D engine



//engine.displayLoadingUI();

        var createScene = function () {



          var scene = new BABYLON.Scene(engine);
      scene.clearColor = new BABYLON.Color3(1, 1, 1);
          var advancedTexture = BABYLON.GUI.AdvancedDynamicTexture.CreateFullscreenUI('myUI');




    var ground = BABYLON.Mesh.CreateGround("ground", 62400, 62400, 0, scene);

    var gl = new BABYLON.GlowLayer("glow", scene);
    gl.intensity = 0.7;


var camera = new BABYLON.ArcRotateCamera('camera1', -Math.PI/2, Math.PI/4, 80, new BABYLON.Vector3(0, 0, 0), scene);
          camera.attachControl(canvas, true);
          camera.wheelDeltaPercentage = .02;
          camera.wheelPrecision = 100;
        //  camera.pinchPrecision = 2;
          camera.useNaturalPinchZoom = true;
          camera.maxZ = 500000;
          camera.alpha = .785;
          camera.beta = .9;
          camera.radius = 6000;
          camera.panningSensibility = 5;
        //  camera.orthoLeft = -12480
      //    camera.orthoRight = 12480
      //    camera.orthoTop = 12480
      //    camera.orthoBottom = -12480


var light = new BABYLON.HemisphericLight('light1', new BABYLON.Vector3(1, 1, 0), scene);
          light.intensity = 0.4;



matGlass = new BABYLON.StandardMaterial('kosh5', scene);
          matGlass.diffuseColor = new BABYLON.Color3(0.36, 0.75, 0.87);
          matGlass.reflectionTexture = new BABYLON.CubeTexture('https://playground.babylonjs.com/textures/TropicalSunnyDay', scene);
          matGlass.reflectionTexture.level = .5;
          matGlass.specularPower = 150;
          matGlass.emissiveColor = new BABYLON.Color3(0.05, 0.05, 0.05);
          matGlass.alpha = 0.15;

groundMat = new BABYLON.StandardMaterial("groundmaterial", scene);
         groundMat.diffuseTexture = "";
        //  groundMat.diffuseTexture = new BABYLON.Texture("https://i.imgur.com/stIKCRV.jpg", scene);
        console.log('All white theme loaded')
       groundMat.diffuseColor = new BABYLON.Color3(1,1,1);
        groundMat.diffuseTexture.uScale = 400.0;
        groundMat.diffuseTexture.vScale = 400.0;
        groundMat.color = new BABYLON.Color3(0,0,0);
        groundMat.alpha = .1;
        ground.material = groundMat;
        ground.rotation.y -=(Math.PI / 2);
        const axes = new BABYLON.AxesViewer(scene, 100)


  var LightMode = 1;

BABYLON.Scene.LongPressDelay = 500;






/*
let textTop = new BABYLON.GUI.TextBlock();
  textTop.text = "Use the buttons to add, remove, and rotate panels.";
  textTop.color = "white";
  textTop.fontSize = 24;
  textTop.verticalAlignment = BABYLON.GUI.Control.VERTICAL_ALIGNMENT_TOP;
  advancedTexture.addControl(textTop);
*/

let btn24Add = BABYLON.GUI.Button.CreateSimpleButton('btn24Add', '24"');
  btn24Add.width = 0.05;
  btn24Add.height = '40px';
  btn24Add.color = 'white';
  btn24Add.background = 'black';
  btn24Add.horizontalAlignment = BABYLON.GUI.Control.HORIZONTAL_ALIGNMENT_LEFT;
  btn24Add.verticalAlignment = BABYLON.GUI.Control.VERTICAL_ALIGNMENT_BOTTOM;
  btn24Add.top = '-170px';
  btn24Add.onPointerClickObservable.add(add24Panel)
  advancedTexture.addControl(btn24Add);

let btn36Add = BABYLON.GUI.Button.CreateSimpleButton('btn36Add', '36"');
  btn36Add.width = 0.05;
  btn36Add.height = '40px';
  btn36Add.color = 'white';
  btn36Add.background = 'black';
  btn36Add.horizontalAlignment = BABYLON.GUI.Control.HORIZONTAL_ALIGNMENT_LEFT;
  btn36Add.verticalAlignment = BABYLON.GUI.Control.VERTICAL_ALIGNMENT_BOTTOM;
  btn36Add.top = '-130px';
  btn36Add.onPointerClickObservable.add(add36Panel)
  advancedTexture.addControl(btn36Add);

let btn42Add = BABYLON.GUI.Button.CreateSimpleButton('btn42Add', '42"');
  btn42Add.width = 0.05;
  btn42Add.height = '40px';
  btn42Add.color = 'white';
  btn42Add.background = 'black';
  btn42Add.horizontalAlignment = BABYLON.GUI.Control.HORIZONTAL_ALIGNMENT_LEFT;
  btn42Add.verticalAlignment = BABYLON.GUI.Control.VERTICAL_ALIGNMENT_BOTTOM;
  btn42Add.top = '-90px';
  btn42Add.onPointerClickObservable.add(add42Panel)
  advancedTexture.addControl(btn42Add);

let btn48Add = BABYLON.GUI.Button.CreateSimpleButton('btn48Add', '48"');
  btn48Add.width = 0.05;
  btn48Add.height = '40px';
  btn48Add.color = 'white';
  btn48Add.background = 'black';
  btn48Add.horizontalAlignment = BABYLON.GUI.Control.HORIZONTAL_ALIGNMENT_LEFT;
  btn48Add.verticalAlignment = BABYLON.GUI.Control.VERTICAL_ALIGNMENT_BOTTOM;
  btn48Add.top = '-50px';
  btn48Add.onPointerClickObservable.add(add48Panel)
  advancedTexture.addControl(btn48Add);

let btn54Add = BABYLON.GUI.Button.CreateSimpleButton('btn54Add', '54"');
  btn54Add.width = 0.05;
  btn54Add.height = '40px';
  btn54Add.color = 'white';
  btn54Add.background = 'black';
  btn54Add.horizontalAlignment = BABYLON.GUI.Control.HORIZONTAL_ALIGNMENT_LEFT;
  btn54Add.verticalAlignment = BABYLON.GUI.Control.VERTICAL_ALIGNMENT_BOTTOM;
  btn54Add.top = '-10px';
  btn54Add.onPointerClickObservable.add(add54Panel)
  advancedTexture.addControl(btn54Add);

let btnLightMode = BABYLON.GUI.Button.CreateSimpleButton('btnLightMode', 'Change Theme');
    btnLightMode.width = 0.07;
    btnLightMode.height = '40px';
    btnLightMode.color = 'white';
    btnLightMode.background = 'black';
    btnLightMode.horizontalAlignment = BABYLON.GUI.Control.HORIZONTAL_ALIGNMENT_RIGHT;
    btnLightMode.verticalAlignment = BABYLON.GUI.Control.VERTICAL_ALIGNMENT_BOTTOM;
    btnLightMode.top = '-10px';
    btnLightMode.onPointerClickObservable.add(switchLightMode)
    advancedTexture.addControl(btnLightMode);
    btnLightMode.fontSize = 14;

/*
let btnAlignPanels = BABYLON.GUI.Button.CreateSimpleButton('btnAlignPanels', 'Align');
    btnAlignPanels.width = 0.07;
    btnAlignPanels.height = '40px';
    btnAlignPanels.color = 'white';
    btnAlignPanels.background = 'black';
    btnAlignPanels.horizontalAlignment = BABYLON.GUI.Control.HORIZONTAL_ALIGNMENT_CENTER;
    btnAlignPanels.verticalAlignment = BABYLON.GUI.Control.VERTICAL_ALIGNMENT_BOTTOM;
    btnAlignPanels.top = '-10px';
    btnAlignPanels.onPointerClickObservable.add(fnAlign)
    advancedTexture.addControl(btnAlignPanels);
    btnAlignPanels.fontSize = 14;
*/
/*
let btnRotate45 = BABYLON.GUI.Button.CreateSimpleButton('btnRotate45', 'Rotate 45');
    btnRotate45.width = 0.07;
    btnRotate45.height = '40px';
    btnRotate45.color = 'white';
    btnRotate45.background = 'black';
    btnRotate45.horizontalAlignment = BABYLON.GUI.Control.HORIZONTAL_ALIGNMENT_CENTER;
    btnRotate45.verticalAlignment = BABYLON.GUI.Control.VERTICAL_ALIGNMENT_BOTTOM;
    btnRotate45.top = '-50px';
  btnRotate45.onPointerClickObservable.add(panRotate45)
    advancedTexture.addControl(btnRotate45);
    btnRotate45.fontSize = 14;

let btnRotate5 = BABYLON.GUI.Button.CreateSimpleButton('btnRotate5', 'Rotate 5');
        btnRotate5.width = 0.07;
        btnRotate5.height = '40px';
        btnRotate5.color = 'white';
        btnRotate5.background = 'black';
        btnRotate5.horizontalAlignment = BABYLON.GUI.Control.HORIZONTAL_ALIGNMENT_CENTER;
        btnRotate5.verticalAlignment = BABYLON.GUI.Control.VERTICAL_ALIGNMENT_BOTTOM;
        btnRotate5.top = '-90px';
      btnRotate5.onPointerClickObservable.add(panRotate5)
        advancedTexture.addControl(btnRotate5);
        btnRotate5.fontSize = 14;
*/

let btnStepUp = BABYLON.GUI.Button.CreateSimpleButton('btnStepUp', 'Step Up');
        btnStepUp.width = 0.07;
        btnStepUp.height = '40px';
        btnStepUp.color = 'white';
        btnStepUp.background = 'black';
        btnStepUp.horizontalAlignment = BABYLON.GUI.Control.HORIZONTAL_ALIGNMENT_CENTER;
        btnStepUp.verticalAlignment = BABYLON.GUI.Control.VERTICAL_ALIGNMENT_BOTTOM;
        btnStepUp.top = '-50px';
        btnStepUp.onPointerClickObservable.add(function(){FloorHeight += 195});
        advancedTexture.addControl(btnStepUp);
        btnStepUp.fontSize = 14;

let btnStepDown = BABYLON.GUI.Button.CreateSimpleButton('btnStepDown', 'Step Down');
                btnStepDown.width = 0.07;
                btnStepDown.height = '40px';
                btnStepDown.color = 'white';
                btnStepDown.background = 'black';
                btnStepDown.horizontalAlignment = BABYLON.GUI.Control.HORIZONTAL_ALIGNMENT_CENTER;
                btnStepDown.verticalAlignment = BABYLON.GUI.Control.VERTICAL_ALIGNMENT_BOTTOM;
                btnStepDown.top = '-10px';
              btnStepDown.onPointerClickObservable.add(function(){FloorHeight -= 195});
                advancedTexture.addControl(btnStepDown);
                btnStepDown.fontSize = 14;


let btnInstructions = BABYLON.GUI.Button.CreateSimpleButton('btnInstructions', 'Click and hold to delete, double click for 11.25 deg turn ');
                btnInstructions.width = 0.8;
                btnInstructions.height = '40px';
                btnInstructions.color = 'black';
                btnInstructions.background = 'white';
                btnInstructions.horizontalAlignment = BABYLON.GUI.Control.HORIZONTAL_ALIGNMENT_CENTER;
                btnInstructions.verticalAlignment = BABYLON.GUI.Control.VERTICAL_ALIGNMENT_TOP;
                btnInstructions.top = '-3px';
          //    btnRotate5.onPointerClickObservable.add(panRotate5)
                advancedTexture.addControl(btnInstructions);
                btnInstructions.fontSize = 14;

/*
let btnChangeView = BABYLON.GUI.Button.CreateSimpleButton('btnChangeView', 'Switch View');
                                btnChangeView.width = 0.1;
                                btnChangeView.height = '38px';
                                btnChangeView.color = 'white';
                                btnChangeView.background = 'black';
                                btnChangeView.horizontalAlignment = BABYLON.GUI.Control.HORIZONTAL_ALIGNMENT_LEFT;
                                btnChangeView.verticalAlignment = BABYLON.GUI.Control.VERTICAL_ALIGNMENT_TOP;
                                btnChangeView.top = '0px';
                                btnChangeView.onPointerClickObservable.add(function(){
                                //camera.mode = BABYLON.Camera.ORTHOGRAPHIC_CAMERA;
                                camera.rotation = new BABYLON.Vector3(1000, 0, 0);
                                });
                                advancedTexture.addControl(btnChangeView);
                                btnChangeView.fontSize = 14;

*/
var allPanels = [];
var FloorHeight = 0;

function fnAlign(){
   //  allPanels[allPanels.length-1].dispose();
    for (var index = 0; index < (allPanels.length); index++) {
   allPanels[index].position.x =( 13*(Math.round(allPanels[index].position.x/13)))

  allPanels[index].position.z =( 13*(Math.round(allPanels[index].position.z/13)))
  }
   //  allPanels.pop()

   }

function add24Panel(){
    //      disc.depth += (624+13)
      var pan2434 = [];
          pan2434 = BABYLON.MeshBuilder.CreateBox('pan2434', {width:13, height: 884, depth: 624}, scene);
                    var scale = 1
          pan2434.position.x = 0
          pan2434.position.z = 0
          pan2434.position.y = 494 + FloorHeight
          pan2434.material = matGlass;
          gl.addIncludedOnlyMesh(pan2434)
          allPanels.push(pan2434)


              pan2434.actionManager = new BABYLON.ActionManager(scene);
              pan2434.actionManager.registerAction(new BABYLON.ExecuteCodeAction(BABYLON.ActionManager.OnLongPressTrigger, function() { pan2434.dispose();              }))
              pan2434.actionManager.registerAction(new BABYLON.ExecuteCodeAction(BABYLON.ActionManager.OnDoublePickTrigger, function() {pan2434.rotation.y -=(Math.PI / 16) ;}))


          var spigot1 = BABYLON.SceneLoader.ImportMesh('', 'https://raw.githubusercontent.com/schmitty421/BabylonSpartan/main/', 'spigot-black.obj', scene,

                   function (newSpigots) {
                      var mesh = newSpigots[0];

                      mesh.isVisible = false;
                      for (var index = 0; index < 1; index++) {
                          var spigCopy = mesh.createInstance('i' + index);
                          spigCopy.isPickable = false;
                          spigCopy.parent = pan2434;
                          spigCopy.position.x = -50;
                          spigCopy.position.y = -498;
                          spigCopy.position.z = -206;
                          spigCopy.position.set(-50,-498,-206);
                          spigCopy.isPickable = false;
                          spigCopy.checkCollisions = false;
                      }
                      for (var index = 0; index < 1; index++) {
                          var spigCopy1 = mesh.createInstance('i' + index);
                          spigCopy1.parent = pan2434;
                          spigCopy1.position.x = -50;
                          spigCopy1.position.y = -498;
                          spigCopy1.position.z = 106;
                      }
                    }
                  );

          }

function add36Panel(){
          //      disc.depth += (636+13)
            var pan3634 = [];
                pan3634 = BABYLON.MeshBuilder.CreateBox('pan3634', {width:13, height: 884, depth: 936}, scene);
                var scale = 1
                pan3634.position.x = 0
                pan3634.position.z = 0
                pan3634.position.y = 494 + FloorHeight
                pan3634.material = matGlass;
                allPanels.push(pan3634)

                pan3634.actionManager = new BABYLON.ActionManager(scene);
                pan3634.actionManager.registerAction(new BABYLON.ExecuteCodeAction(BABYLON.ActionManager.OnLongPressTrigger, function() { pan3634.dispose();              }))
                pan3634.actionManager.registerAction(new BABYLON.ExecuteCodeAction(BABYLON.ActionManager.OnDoublePickTrigger, function() {pan3634.rotation.y -=(Math.PI / 16) ;}))

                console.log(allPanels.length+' allPanels length')


                var spigot1 = BABYLON.SceneLoader.ImportMesh('', 'https://raw.githubusercontent.com/schmitty421/BabylonSpartan/main/',
                      'spigot-black.obj', scene,

                         function (newSpigots) {
                            var mesh = newSpigots[0];

                            mesh.isVisible = false;
                            for (var index = 0; index < 1; index++) {
                                var spigCopy = mesh.createInstance('i' + index);

                                spigCopy.parent = pan3634;
                                spigCopy.position.x = -50;
                                spigCopy.position.y = -498;
                                spigCopy.position.z = -284;

                            }
                            for (var index = 0; index < 1; index++) {
                                var spigCopy1 = mesh.createInstance('i' + index);

                                spigCopy1.parent = pan3634;
                                spigCopy1.position.x = -50;
                                spigCopy1.position.y = -498;
                                spigCopy1.position.z = 184
                            }
                          }
                        );

                }

function add42Panel(){
                //      disc.depth += (642+13)
                  var pan4234 = [];
                      pan4234 = BABYLON.MeshBuilder.CreateBox('pan4234', {width:13, height: 884, depth: 1092}, scene);
                      var scale = 1
                      pan4234.position.x = 0
                      pan4234.position.z = 0
                      pan4234.position.y = 494 + FloorHeight
                      pan4234.material = matGlass;
                      allPanels.push(pan4234)
                      pan4234.actionManager = new BABYLON.ActionManager(scene);
                      pan4234.actionManager.registerAction(new BABYLON.ExecuteCodeAction(BABYLON.ActionManager.OnLongPressTrigger, function() { pan4234.dispose();              }))
                      pan4234.actionManager.registerAction(new BABYLON.ExecuteCodeAction(BABYLON.ActionManager.OnDoublePickTrigger, function() {pan4234.rotation.y -=(Math.PI / 16) ;}))
                      console.log(allPanels.length+' allPanels length')


                      var spigot1 = BABYLON.SceneLoader.ImportMesh('', 'https://raw.githubusercontent.com/schmitty421/BabylonSpartan/main/',
                              'spigot-black.obj', scene,

                               function (newSpigots) {
                                  var mesh = newSpigots[0];

                                  mesh.isVisible = false;
                                  for (var index = 0; index < 1; index++) {
                                      var spigCopy = mesh.createInstance('i' + index);

                                      spigCopy.parent = pan4234;
                                      spigCopy.position.x = -50;
                                      spigCopy.position.y = -498;
                                      spigCopy.position.z = -323;

                                  }
                                  for (var index = 0; index < 1; index++) {
                                      var spigCopy1 = mesh.createInstance('i' + index);

                                      spigCopy1.parent = pan4234;
                                      spigCopy1.position.x = -50;
                                      spigCopy1.position.y = -498;
                                      spigCopy1.position.z = 223;
                                  }
                                }
                              );

                      }

function add48Panel(){
                                      //      disc.depth += (648+13)
                                        var pan4834 = [];
                                            pan4834 = BABYLON.MeshBuilder.CreateBox('pan4834', {width:13, height: 884, depth: 1248}, scene);
                                            var scale = 1
                                            pan4834.position.x = 0
                                            pan4834.position.z = 0
                                            pan4834.position.y = 494 + FloorHeight
                                            pan4834.material = matGlass;
                                            allPanels.push(pan4834)
                                            pan4834.actionManager = new BABYLON.ActionManager(scene);
                                            pan4834.actionManager.registerAction(new BABYLON.ExecuteCodeAction(BABYLON.ActionManager.OnLongPressTrigger, function() { pan4834.dispose();              }))
                                            pan4834.actionManager.registerAction(new BABYLON.ExecuteCodeAction(BABYLON.ActionManager.OnDoublePickTrigger, function() {pan4834.rotation.y -=(Math.PI / 16) ;}))
                                            console.log(allPanels.length+' allPanels length')


                                            var spigot1 = BABYLON.SceneLoader.ImportMesh('', 'https://raw.githubusercontent.com/schmitty421/BabylonSpartan/main/',
                                                      'spigot-black.obj', scene,

                                                     function (newSpigots) {
                                                        var mesh = newSpigots[0];

                                                        mesh.isVisible = false;
                                                        for (var index = 0; index < 1; index++) {
                                                            var spigCopy = mesh.createInstance('i' + index);

                                                            spigCopy.parent = pan4834;
                                                            spigCopy.position.x = -50;
                                                            spigCopy.position.y = -498 ;
                                                            spigCopy.position.z = -362;

                                                        }
                                                        for (var index = 0; index < 1; index++) {
                                                            var spigCopy1 = mesh.createInstance('i' + index);

                                                            spigCopy1.parent = pan4834;
                                                            spigCopy1.position.x = -50;
                                                            spigCopy1.position.y = -498;
                                                            spigCopy1.position.z = 262;
                                                        }
                                                      }
                                                    );

                                            }

function add54Panel(){
                                            //      disc.depth += (654+13)
                                              var pan5434 = [];
                                                  pan5434 = BABYLON.MeshBuilder.CreateBox('pan5434', {width:13, height: 884, depth: 1404}, scene);
                                                  var scale = 1
                                                  pan5434.position.x = 0
                                                  pan5434.position.z = 0
                                                  pan5434.position.y = 494 + FloorHeight
                                                  pan5434.material = matGlass;
                                                  allPanels.push(pan5434)
                                                  pan5434.actionManager = new BABYLON.ActionManager(scene);
                                                  pan5434.actionManager.registerAction(new BABYLON.ExecuteCodeAction(BABYLON.ActionManager.OnLongPressTrigger, function() { pan5434.dispose();              }))
                                                  pan5434.actionManager.registerAction(new BABYLON.ExecuteCodeAction(BABYLON.ActionManager.OnDoublePickTrigger, function() {pan5434.rotation.y -=(Math.PI / 16) ;}))
                                                  console.log(allPanels.length+' allPanels length')


                                                  var spigot1 = BABYLON.SceneLoader.ImportMesh('', 'https://raw.githubusercontent.com/schmitty421/BabylonSpartan/main/',
                                                          'spigot-black.obj', scene,

                                                           function (newSpigots) {
                                                              var mesh = newSpigots[0];

                                                              mesh.isVisible = false;
                                                              for (var index = 0; index < 1; index++) {
                                                                  var spigCopy = mesh.createInstance('i' + index);

                                                                  spigCopy.parent = pan5434;
                                                                  spigCopy.position.x = -50;
                                                                  spigCopy.position.y = -498;
                                                                  spigCopy.position.z = -518;

                                                              }
                                                              for (var index = 0; index < 1; index++) {
                                                                  var spigCopy1 = mesh.createInstance('i' + index);

                                                                  spigCopy1.parent = pan5434;
                                                                  spigCopy1.position.x = -50;
                                                                  spigCopy1.position.y = -498;
                                                                  spigCopy1.position.z = -50;
                                                              }
                                                              for (var index = 0; index < 1; index++) {
                                                                  var spigCopy2 = mesh.createInstance('i' + index);

                                                                  spigCopy2.parent = pan5434;
                                                                  spigCopy2.position.x = -50;
                                                                  spigCopy2.position.y = -498;
                                                                  spigCopy2.position.z = 418;
                                                              }
                                                            }
                                                          );

                                                  }

function switchLightMode() {
  if (LightMode === 0) {
    console.log('All white theme loaded')
    scene.clearColor = new BABYLON.Color3(1, 1, 1);
    matGlass.reflectionTexture = new BABYLON.CubeTexture('https://playground.babylonjs.com/textures/TropicalSunnyDay', scene);
    matGlass.alpha = 0.15;
    groundMat.diffuseTexture = "";
    groundMat.diffuseTexture.uScale = 400.0;
    groundMat.diffuseTexture.vScale = 400.0;
    groundMat.color = new BABYLON.Color3(0,0,0);
    groundMat.diffuseColor = new BABYLON.Color3(1,1,1);
            groundMat.alpha = .1;
    ground.material = groundMat;
    LightMode = 1;
    return;


  }
  else if (LightMode === 1) {
    console.log('Mahogany decking theme loaded')
    scene.clearColor = new BABYLON.Color3(1, 1, 1);
    matGlass.reflectionTexture = new BABYLON.CubeTexture('https://playground.babylonjs.com/textures/TropicalSunnyDay', scene);
    matGlass.alpha = 0.15;
    groundMat.diffuseTexture = new BABYLON.Texture("https://i.imgur.com/gb1Ds76.jpg", scene);
    groundMat.diffuseTexture.uScale = 400.0;
    groundMat.diffuseTexture.vScale = 400.0;
    groundMat.alpha = 1;
  groundMat.diffuseColor = new BABYLON.Color3(240/253, 223/255, 203/255);
  ground.material = groundMat;
    LightMode = 2;
    return;
    }

  else if (LightMode === 2) {
     console.log('White Oak spartan theme loaded')
     scene.clearColor = new BABYLON.Color3(1, 1, 1);
       matGlass.reflectionTexture = new BABYLON.CubeTexture('https://playground.babylonjs.com/textures/TropicalSunnyDay', scene);
                 matGlass.alpha = 0.15;
     groundMat.diffuseTexture = new BABYLON.Texture("https://i.imgur.com/QjFjJ7r.jpg", scene);
     groundMat.diffuseTexture.uScale = 400.0;
     groundMat.diffuseTexture.vScale = 400.0;
     groundMat.alpha = 1;
   groundMat.diffuseColor = new BABYLON.Color3(1,1,1);
   ground.material = groundMat;
     LightMode = 3;
      return;
    }


 else if (LightMode === 3) {
   console.log('White spartan theme loaded')
   scene.clearColor = new BABYLON.Color3(1, 1, 1);
     matGlass.reflectionTexture = new BABYLON.CubeTexture('https://playground.babylonjs.com/textures/TropicalSunnyDay', scene);
               matGlass.alpha = 0.15;
   groundMat.diffuseTexture = new BABYLON.Texture("https://i.imgur.com/Qd2IaBo.jpg", scene);
   groundMat.diffuseTexture.uScale = 400.0;
   groundMat.diffuseTexture.vScale = 400.0;
        groundMat.alpha = .5;
 groundMat.diffuseColor = new BABYLON.Color3(1,1,1);
 ground.material = groundMat;
   LightMode = 4;
    return;
  }

  else if (LightMode === 4) {
   console.log('Black spartan theme loaded')
    scene.clearColor = new BABYLON.Color3(0, 0, 0);
    matGlass.reflectionTexture = new BABYLON.CubeTexture('https://playground.babylonjs.com/textures/TropicalSunnyDay', scene);
              matGlass.alpha = 0.15;
    groundMat.diffuseTexture = new BABYLON.Texture("https://i.imgur.com/stIKCRV.jpg", scene);
    groundMat.diffuseTexture.uScale = 400.0;
    groundMat.diffuseTexture.vScale = 400.0;
         groundMat.alpha = 1;
  groundMat.diffuseColor = new BABYLON.Color3(1,1,1);
  ground.material = groundMat;
    LightMode = 5;
    return;
    }
    else if (LightMode === 5) {
     console.log('Grid theme loaded')
      scene.clearColor = new BABYLON.Color3(1,1,1);
      matGlass.reflectionTexture = new BABYLON.CubeTexture('https://playground.babylonjs.com/textures/TropicalSunnyDay', scene);
      matGlass.alpha = 0.5;
      groundMat.diffuseTexture = new BABYLON.Texture("https://i.imgur.com/WKDV94r.jpg", scene);
      groundMat.diffuseTexture.uScale = 400.0;
      groundMat.diffuseTexture.vScale = 400.0;
    groundMat.diffuseColor = new BABYLON.Color3(1,1,1);
    groundMat.alpha = 1;
    ground.material = groundMat;
    var downlight = new BABYLON.DirectionalLight("DirectionalLight", new BABYLON.Vector3(0, 1, 0), scene);
    downlight.intensity = 0.2;

      LightMode = 0;
      return;


      }



    }



function panRotate45() {
   allPanels[allPanels.length-1].rotation.y -=(Math.PI / 4);
  //allPanels[2].rotation.y -=(Math.PI / 4);
          }

function panRotate5() {
          allPanels[allPanels.length-1].rotation.y -=(Math.PI / 36);

                    }


        // Events


var startingPoint;
var currentMesh;

var getGroundPosition = function () {
            // Use a predicate to get position on the ground
            var pickinfo = scene.pick(scene.pointerX, scene.pointerY, function (mesh) { return mesh == ground; });
            if (pickinfo.hit) {
              console.log('mouse on object')
                return pickinfo.pickedPoint;

            }
            return null;
        }



var onPointerDown = function (evt) {
            if (evt.button !== 0) {

                return;
            }

            // check if we are under a mesh
  var pickInfo = scene.pick(scene.pointerX, scene.pointerY, function (mesh) {
    console.log('pointer downclick')
                    return mesh !== ground;
                });

  if (pickInfo.hit) {
      currentMesh = pickInfo.pickedMesh;
      startingPoint = getGroundPosition(evt);
      console.log(currentMesh.id)
                if (startingPoint) { // we need to disconnect camera from canvas
                    setTimeout(function () {
                        camera.detachControl(canvas);
                    }, 0);
                }
            }
        }



var onPointerUp = function () {
        fnAlign();
              if (startingPoint) {
                console.log('pointer upclick')
                camera.attachControl(canvas, true);
                startingPoint = null;
                return;
            }
        }

var onPointerMove = function (evt) {
            if (!startingPoint) {
                return;
            }
            var current = getGroundPosition(evt);
            if (!current) {
                return;
            }
            var diff = current.subtract(startingPoint);


            if(evt.ctrlKey){

            }else{
                currentMesh.position.addInPlace(diff);
                startingPoint = current;
                var myPoints = [
                    currentMesh.position,
              //      currentMesh.other.position
                ];
                line = BABYLON.MeshBuilder.CreateLines("lines", {points: myPoints, instance: currentMesh.line});
            }

        }

canvas.addEventListener("pointerdown", onPointerDown, false);
canvas.addEventListener("pointerup", onPointerUp, false);
canvas.addEventListener("pointermove", onPointerMove, false);

          scene.registerAfterRender(function () {


          })



            return scene;
        };

        var scene = createScene(); //Call the createScene function

        // Register a render loop to repeatedly render the scene
        engine.runRenderLoop(function () {
                scene.render();
        });

        window.addEventListener('resize', function () {
                engine.resize();
        });


