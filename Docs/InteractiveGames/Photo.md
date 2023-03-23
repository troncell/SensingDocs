# 体感拍照设置
#  AppSetting.xml介绍
开发提供KinectShot文件包，在文件夹下settings文件夹里有AppSetting.xml文件

```
<?xml version="1.0" encoding="utf-8"?>
<Setting>
  <!--App宽度-->
  <DisplayWidth Value="1920">1920</DisplayWidth>
  <!--App高度-->
  <DisplayHeight Value="1080">1080</DisplayHeight>
  <!--启动页面(WelcomePage,MainPage)-->
  <StartPage Value="MainPage">MainPage</StartPage>
  <Debug Value="False">False</Debug>
  <!--一直显示头饰-->
  <AlwaysShowThings Value="True">True</AlwaysShowThings>
  <!--拍照触发区域-->
  <TriggerBounds>
    <!--中心点X(m)-->
    <CenterX Value="0.2">0.2</CenterX>
    <!--中心点Y(m)-->
    <CenterY Value="1.8">1.8</CenterY>
    <!--宽度(m)-->
    <Width Value="1">3</Width>
    <!--高度(m)-->
    <Height Value="1">2</Height>
  </TriggerBounds>
  <!--允许人进入自动拍照-->
  <EnableAutoShot Value="False">False</EnableAutoShot>
  <!--人进入自动拍照时间-->
  <AutoShotTime Value="15">15</AutoShotTime>
  <!--剪刀手手势拍照-->
  <EnableVSign Value="True">True</EnableVSign>
  <!--无人时间-->
  <IdleTime Value="60">60</IdleTime>
  <!--扫码倒计时时间-->
  <ScanTime Value="30">30</ScanTime>
  <!--最近距离-->
  <MinDistance Value="1">0</MinDistance>
  <!--最远距离-->
  <MaxDistance Value="2">3</MaxDistance>
  <!--第一页轮播图(无人广告)-->
  <Ads>
    <!-- <Ad UriKind="Application" FileName="settings/Banner/WpfApp7.exe" Duration="10"/>
     <Ad UriKind="Application" FileName="settings/Banner/banner01.png" /> -->

  </Ads>
  <!--第二页前景图-->
  <Foregrounds>
    <Foreground UriKind="Application" FileName="settings/Foreground/foreground01.png" />
  </Foregrounds>
  <!--第二页轮播图(有人广告)-->
  <!-- <Banners>
    <Banner UriKind="Application" FileName="settings/Banner/banner11.jpg" />

  </Banners> -->
  <!--第二页帽子，修改帽子大小、位置、图片-->
  <ThingGroups>
    <ThingGroup Enable="True">
      <Things>
        <Thing AnchorX="259" AnchorY="633" Scale="2.0" OffsetY="0" ThingType="Hat" MediaType="Image" Enable="True" FrameRate="20">
          <Source UriKind="Application" FileName="settings/Hat/hat01.png" />
        </Thing>
      </Things>
    </ThingGroup>
    <ThingGroup Enable="True">
      <Things>
        <Thing AnchorX="183" AnchorY="288" Scale="1.9" OffsetY="36" ThingType="Hat" MediaType="Image" Enable="True" FrameRate="20">
          <Source UriKind="Application" FileName="settings/Hat/hat2.png" />
        </Thing>
      </Things>
    </ThingGroup>
    <ThingGroup Enable="True">
      <Things>
        <Thing AnchorX="216" AnchorY="150" Scale="1.8" OffsetY="0" ThingType="Hat" MediaType="Image" Enable="True" FrameRate="20">
          <Source UriKind="Application" FileName="settings/Hat/hat5.png" />
        </Thing>
      </Things>
    </ThingGroup>
    <ThingGroup Enable="True">
      <Things>
        <Thing AnchorX="242" AnchorY="550" Scale="2.0" OffsetY="0" ThingType="Hat" MediaType="Image" Enable="True" FrameRate="20">
          <Source UriKind="Application" FileName="settings/Hat/hat4.png" />
        </Thing>
      </Things>
    </ThingGroup>
    <ThingGroup Enable="True">
      <Things>
        <Thing AnchorX="1409" AnchorY="1070" Scale="3.6" OffsetY="0" ThingType="Hat" MediaType="Image" Enable="True" FrameRate="20">
          <Source UriKind="Application" FileName="settings/Hat/hat7.png" />
        </Thing>
      </Things>
    </ThingGroup>
    <ThingGroup Enable="False">
      <Things>
        <Thing AnchorX="134" AnchorY="170" Scale="2.2" OffsetY="-10" ThingType="Hat" MediaType="Image" Enable="True" FrameRate="20">
          <Source UriKind="Application" FileName="settings/Hat/hat18.png" />
        </Thing>
      </Things>
    </ThingGroup>


  </ThingGroups>
  <!--拍照声音-->
  <CachaSound UriKind="Application" FileName="settings/Sound/cacha.wav" />
  <!--背景声音-->
  <BGSound UriKind="Application" FileName="settings/Sound/bg.wav" />
  <!--倒计时声音-->
  <CountdownSound UriKind="Application" FileName="settings/Sound/321.wav" />
  <!--生成照片页面的背景图、大小-->
  <ScanPage>
    <Canvas Width="1920" Height="1080">
      <Controls>
        <Border Width="1920" Height="1080" Background="Black" Opacity="0.91" />
        <Image Height="1080" Width="1920">
          <FileSource Path="settings\Foreground\bg.png" />
        </Image>
        <!-- <KinectRegion Width="1920" Height="1080" ZIndex="10">
          <HandImageSource Path="settings\Images\hand.png" />
          <Controls>
           
</Controls>
        </KinectRegion>
        <!-- 生成照片页面关闭弹框按钮 -->
        <ImageButton Name="closeButton" Width="65" Height="65" Left="1383" Top="664">
          <FileSource Path="settings\Images\close.png" />
        </ImageButton>
        <!-- 生成照片页面会首页按钮 -->
        <ImageButton Name="exitButton" Width="66" Height="66" Left="1478" Top="664">
          <FileSource Path="settings\Images\home.png" />
        </ImageButton>

<!-- 手机预览画面 -->
 <Border Name="phonePreview" Background="#d9a66a" BorderBrush="#d9a66a" BorderThickness="1,1,1,1" Width="1070" Height="603" Left="276" Top="228" CornerRadius="0" />
        <Canvas Width="1920" Height="1080">
          <Controls>
            <!-- <Image Height="348" Width="236">
              <FileSource Path="settings\Images\qrcodebg.png" />
            </Image> -->
            <Image Name="qrcode" QrcodeUrl="" Width="116" Height="116" Left="1408" Top="395" />
            <SprocketControl Name="qrcoderProgress" Visibility="Collapsed" TickColor="Black" Width="130" Height="130" TickWidth="3" TickCount="12" StartAngle="-90" IsIndeterminate="True" Interval="60" LowestAlpha="50" AlphaTicksPercentage="50" TickStyle="Triangle" InnerRadius="0.3" OuterRadius="0.5" Left="59" Top="75" />
            <TextBlock Name="countDownText" Width="80" Height="80" TextAlignment="Left" Left="1423" Top="320" HorizontalAlignment="Center" Text="" FontSize="40" Foreground="#3583df" CultureInfo="GongFanMianFeiTi2.0" />
            <!-- <CustomElement Width="1072" Height="40" Left="243" Top="886">
              <ActivatorInfo AssemblyFile="settings\Animation\tishi.exe" TypeName="tishi.UserControl2" />
            </CustomElement> -->
          </Controls>
        </Canvas>
        <Border Name="message" Opacity="0" Background="#88000000" Left="693" Top="795" Padding="10" Width="430">
          <Child>
            <TextBlock Name="messageText" HorizontalAlignment="Center" Text="aaa" FontSize="60" Foreground="White" />
          </Child>
        </Border>
      </Controls>
    </Canvas>
  </ScanPage>
  <!--MainPage-->
  <MainPage>
    <Canvas Width="1920" Height="1080">
      <Controls>
        <Canvas Name="preview" Height="1080" Width="1920" ClipToBounds="True">
          <Controls>
            <Canvas Name="animationLayer" Width="1920" Height="1080">
              <Controls>
                <Image Name="colorImage" Width="1920" Height="1080" />
              </Controls>
            </Canvas>
            <Banner Name="foregoundPlayer" UseTransition="False" SelectedIndex="0" Interval="86400" Width="1920" Height="1080" Opacity="0"/>
            <Image Left="0" Top="0" Name="overlayImage" Width="1920" Height="1080" Opacity="0">
              <FileSource Path="settings/Foreground/foreground01.png" />

  </Image>
            <!-- <Banner Name="bannerPlayer" SelectedIndex="0" Interval="86400" Width="626" Height="1080" Left="1294" /> -->
            <CustomElement Name="countdownAnimation" Width="1920" Height="1080">
              <ActivatorInfo AssemblyFile="settings\Animation\daojishi.exe" TypeName="daojishi.UserControl1" />
            </CustomElement>
            <!--<MediaElement Name="fallingLeaves" Width="1920" Height="2160">
              <FileSource Path="Assets/flower.wmv"/>
              <Effect>
                <AlphaMaskEffect />
              </Effect>
            </MediaElement>-->
          </Controls>
        </Canvas>
        <!-- <CustomElement Width="1920" Height="1080">
          <ActivatorInfo AssemblyFile="settings\Animation\jiandaoshsou.exe" TypeName="jiandaoshsou.UserControl1" />
        </CustomElement> -->
        <!-- <CustomElement Width="372" Height="139" Left="0" Top="80">
          <ActivatorInfo AssemblyFile="settings\Animation\shou01.exe" TypeName="shou01.UserControl1" />
        </CustomElement> -->
        <!-- <CustomElement Width="1920" Height="1080" Left="0" Top="0">
          <ActivatorInfo AssemblyFile="settings\Animation\tishi1.exe" TypeName="tishi1.UserControl1" />
        </CustomElement> -->
        <CustomElement Width="1920" Height="1080" Left="0" Top="0">
          <ActivatorInfo AssemblyFile="settings\Animation\tishi.exe" TypeName="tishi.UserControl1" />
        </CustomElement>
        <CustomElement Width="1920" Height="1080" Left="0" Top="0">
          <ActivatorInfo AssemblyFile="settings\Animation\yingcaidonghua.exe" TypeName="yingcaidonghua.UserControl1" />
        </CustomElement>
        <!-- <Image Height="151" Width="1920">
          <FileSource Path="settings\Images\2.png" />
        </Image> -->
        <Button Name="shotButton" Width="100" Height="100" Opacity="0" Right="0" Bottom="0" Content="拍照" Click="ClickShot" />
        <LongPressButton Name="showSettingButton" Width="100" Height="100" Opacity="0" Left="0" Bottom="0" Content="菜单显示" />
        <Canvas Name="settingPanel" Width="1920" Height="1080" IsShow="false" Left="0" Top="0">
          <Controls>
            <!-- <Button Name="exitButton" Width="100" Height="50" Content="退出" Bottom="0" Click="ClickExit" /> -->
            <Button Name="hideSettingButton" Width="100" Height="50" Bottom="100" Content="隐藏" Click="ClickExit" />
          </Controls>
        </Canvas>

 <ImageButton Name="exitButton" Width="66" Height="66" Left="10" Top="1000">
          <FileSource Path="settings\Images\home.png" />
        </ImageButton>

</Controls>
    </Canvas>
  </MainPage>
</Setting>

```

# DeviceKeySetting.xml  介绍

```

<?xml version="1.0" encoding="utf-8"?>
<Setting>
  <SubscriptionKey Value="ff12a6a209254b47960876e37f02054d">a14c2f74b9b748909dd6db25f013cf10</SubscriptionKey>
  <SoftwareCode Value="1111">1111</SoftwareCode>
  <!-- 设备mac地址 -->
  <Mac Value="F8633FCDD6AB11">F8633FCDD6AB11</Mac>
  <!-- 设备下游戏密钥 -->
  <DeviceActivityGameSecurityKey Value="1a78ed6edb0e45e08e1e9064ae6ee72c">4789949015454661af2ec3f368c1446f</DeviceActivityGameSecurityKey>
  <!--Taobao或WeChat平台-->
  <EnumSnsType Value="WeChat">WeChat</EnumSnsType>
  <TargetUrl Value=""></TargetUrl>
</Setting>

```