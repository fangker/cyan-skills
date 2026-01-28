# Button 组件

## 概述
基础按钮组件,提供点击功能、禁用状态和多种样式变体。

## API

### Props
- `label`: string - 按钮文字 (必填)
- `onClick`: () => void - 点击事件处理函数 (可选)
- `disabled`: boolean - 是否禁用按钮 (可选,默认 false)
- `variant`: 'primary' | 'secondary' | 'danger' - 按钮样式变体 (可选,默认 'primary')

### 变体说明
- `primary`: 主要操作按钮,蓝色高亮样式
- `secondary`: 次要操作按钮,灰色样式
- `danger`: 危险操作按钮,红色警告样式

## 示例

### 基础用法
```tsx
<Button label="点击我" onClick={handleClick} />
```

### 不同变体
```tsx
<Button label="主要操作" variant="primary" onClick={handlePrimary} />
<Button label="次要操作" variant="secondary" onClick={handleSecondary} />
<Button label="删除" variant="danger" onClick={handleDelete} />
```

### 禁用状态
```tsx
<Button label="禁用按钮" disabled={true} />
```

### 组合使用
```tsx
<Button
  label="确认删除"
  variant="danger"
  disabled={!canDelete}
  onClick={handleDelete}
/>
```
