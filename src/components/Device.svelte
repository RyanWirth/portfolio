<style type="text/scss">
  div {
    position: absolute;
    top: 50%;
    left: 50%;
    width: 100%;
    transform: translate(-50%, -50%);
  }

  img {
    position: absolute;
  }

  .device__frame {
    height: auto;
    max-width: 100%;
    position: relative;
  }

  .device__iphone::before,
  .device__iphone .device__screen {
    top: 7.784431138%;
    left: 16.4021164%;
    width: 66.137566137%;
    height: 80.838323353%;
  }
</style>

<div class="device__iphone">
  <img class="device__screen" src="/images/kenko.jpg" alt="Kenko" />
  <img class="device__frame" src="/images/iphone-x.svg" alt="iPhone X" />
</div>
