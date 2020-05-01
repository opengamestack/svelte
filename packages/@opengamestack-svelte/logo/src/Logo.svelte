<script>
  export let remSize;

  const vars = `--size: ${remSize}rem;
  --circle-size: ${remSize}rem;
  --gamepad-size: ${remSize / 2}rem;
  --gamepad-ty: ${remSize / -6}rem;
  --bars-size: ${remSize / 4}rem;
  --bars-ty: ${remSize / 6}rem;`;
</script>

<style>
  .container {
    position: relative;
    height: var(--size);
    width: var(--size);
  }
  .inner {
    position: absolute;
    height: var(--size);
    width: var(--size);
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
  }
  .icon {
    position: absolute;
    top: 50%;
    left: 50%;
  }
  .icon-circle {
    font-size: var(--circle-size);
    transform: translate(-50%, -50%);
  }
  .icon-gamepad {
    font-size: var(--gamepad-size);
    transform: translate(-50%, -50%) translateY(var(--gamepad-ty));
  }
  .icon-bars {
    font-size: var(--bars-size);
    transform: translate(-50%, -50%) translateY(var(--bars-ty));
  }
</style>

<div class="container" style={vars}>
  <div class="inner">
    <i class="icon icon-circle fal fa-circle" />
    <i class="icon icon-gamepad fas fa-gamepad" />
    <i class="icon icon-bars fas fa-bars" />
  </div>
</div>
